## Tutorial adding to a scene

```julia
using Makie

 x = range(0, stop = 2pi, length = 80)
 f1(x) = sin.(x)
 f2(x) = exp.(-x) .* cos.(2pi*x)
 y1 = f1(x)
 y2 = f2(x)

 scene = lines(x, y1, color = :blue)
 scatter!(scene, x, y1, color = :red, markersize = 0.1)

 lines!(scene, x, y2, color = :black)
 scatter!(scene, x, y2, color = :green, marker = :utriangle, markersize = 0.1)


```
```@raw html

<div style="display:inline-block"><p style="display:inline-block; text-align: center">1<br><img src="/home/sd/ReferenceImages/recordings/tutorial_adding_to_a_scene/media/image.jpg" alt="1<br>">
</p></div>
```