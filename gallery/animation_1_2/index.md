## Animation

```julia
using Makie

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

<div style="display:inline-block"><p style="display:inline-block; text-align: center">1<br><video controls autoplay loop muted>
  <source src="/home/sd/ReferenceImages/recordings/animation_1_2/media/animation_1_2.mp4" type="video/mp4">
  Your browser does not support mp4. Please use a modern browser like Chrome or Firefox.
</video>
</p></div>
```
