## Animation

```julia
using AbstractPlotting

 scene = Scene()
 f(t, v, s) = (sin(v + t) * s, cos(v + t) * s)
 time_node = Node(0.0)
 p1 = scatter!(scene, lift(t-> f.(t, range(0, stop = 2pi, length = 50), 1), time_node))[end]
 p2 = scatter!(scene, lift(t-> f.(t * 2.0, range(0, stop = 2pi, length = 50), 1.5), time_node))[end]
 points = lift(p1[1], p2[1]) do pos1, pos2
     map((a, b)-> (a, b), pos1, pos2)
 end
 linesegments!(scene, points)
 N = 150
 record(scene, "output.mp4", range(0, stop = 10, length = N)) do i
     push!(time_node, i)
end


```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <video controls autoplay loop muted>
  <source src="https://simondanisch.github.io/ReferenceImages/galleryanimation/media/animation.mp4" type="video/mp4">
  Your browser does not support mp4. Please use a modern browser like Chrome or Firefox.
</video>

    </p>
</div>

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="https://simondanisch.github.io/ReferenceImages/galleryanimation/media/thumb.jpg" alt="">

    </p>
</div>

```
