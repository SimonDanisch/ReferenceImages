## GUI for exploring Lorenz equation

```julia
using AbstractPlotting
 using Colors
 using AbstractPlotting: textslider, colorswatch

 s1, a = textslider(0f0:50f0, "a", start = 13)
 s2, b = textslider(-20f0:20f0, "b", start = 10)
 s3, c = textslider(0f0:20f0, "c", start = 2)
 s4, d = textslider(range(0.0, stop = 0.02, length = 100), "d", start = 0.01)
 s5, scales = textslider(range(0.01, stop = 0.5, length = 100), "scale", start = 0.1)
 s6, colorsw, pop = colorswatch()

 function lorenz(t0, a, b, c, h)
     Point3f0(
         t0[1] + h * a * (t0[2] - t0[1]),
         t0[2] + h * (t0[1] * (b - t0[3]) - t0[2]),
         t0[3] + h * (t0[1] * t0[2] - c * t0[3]),
     )
 end
 # step through the `time`
 function lorenz(array::Vector, a = 5.0 ,b = 2.0, c = 6.0, d = 0.01)
     t0 = Point3f0(0.1, 0, 0)
     for i = eachindex(array)
         t0 = lorenz(t0, a,b,c,d)
         array[i] = t0
     end
     array
 end
 n1, n2 = 18, 30
 N = n1*n2
 args_n = (a, b, c, d)
 v0 = lorenz(zeros(Point3f0, N), to_value.(args_n)...)
 positions = lift(lorenz, Node(v0), args_n...)
 rotations = lift(diff, positions)
 rotations = lift(x-> push!(x, x[end]), rotations)

 mesh_scene = meshscatter(
     positions,
     markersize = scales, rotation = rotations,
     intensity = collect(range(0f0, stop = 1f0, length = length(positions[]))),
     color = colorsw
 )
 parent = Scene(resolution = (1000, 800))
 vbox(
     hbox(s1, s2, s3, s4, s5, s6),
     mesh_scene, parent = parent
 )
 RecordEvents(parent, "output")


```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="https://simondanisch.github.io/ReferenceImages/gallerygui_for_exploring_lorenz_equation/media/thumb.jpg" alt="">

    </p>
</div>

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <video controls autoplay loop muted>
  <source src="https://simondanisch.github.io/ReferenceImages/gallerygui_for_exploring_lorenz_equation/media/video.mp4" type="video/mp4">
  Your browser does not support mp4. Please use a modern browser like Chrome or Firefox.
</video>

    </p>
</div>

```
