## sliders

```julia
using AbstractPlotting

 s1 = slider(LinRange(0.01, 1, 100), raw = true, camera = campixel!, start = 0.3)
 s2 = slider(LinRange(-2pi, 2pi, 100), raw = true, camera = campixel!)
 data = lift(s2[end][:value]) do v
     map(LinRange(0, 2pi, 100)) do x
         4f0 .* Point2f0(sin(x) + (sin(x * v) .* 0.1), cos(x) + (cos(x * v) .* 0.1))
     end
 end
 p = scatter(data, markersize = s1[end][:value])

 RecordEvents(
     hbox(p, vbox(s1, s2), parent = Scene(resolution = (500, 500))),
     "output"
 )


```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <video controls autoplay loop muted>
  <source src="https://simondanisch.github.io/ReferenceImages/gallery//sliders/media/video.mp4" type="video/mp4">
  Your browser does not support mp4. Please use a modern browser like Chrome or Firefox.
</video>

    </p>
</div>

```
