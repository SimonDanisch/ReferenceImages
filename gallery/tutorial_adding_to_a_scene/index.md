## Tutorial adding to a scene

```julia
using AbstractPlotting

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

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="https://simondanisch.github.io/ReferenceImages/gallery//tutorial_adding_to_a_scene/media/image.jpg" alt="">

    </p>
</div>

```
