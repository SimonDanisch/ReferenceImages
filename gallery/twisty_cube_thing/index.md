## Twisty cube thing

```julia
using AbstractPlotting, GLMakie, GLMakie

 (a, b) = -1, 2
 r = range(-2, stop = 2, length = 100)
 z = ((x,y) -> x + y).(r, r') ./ 5
 me = [z .* sin.(3 .* (atan.(y ./ x) .+ z.^2 .+ pi .* (x .> 0))) for x=r, y=r, z=r]
 me2 = me .* (me .> z .* 0.25)
 contour(me2, levels = 6, colormap = :Spectral)


```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="https://simondanisch.github.io/ReferenceImages/gallery//twisty_cube_thing/media/image.jpg" alt="">

    </p>
</div>

```
