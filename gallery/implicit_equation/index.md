## Implicit equation

```julia
using AbstractPlotting, GLMakie, GLMakie

 r = range(-5, stop = 5, length = 400)
 (a, b) = -1, 2
 z = ((x,y) -> y.^4 - x.^4 + a .* y.^2 + b .* x.^2).(r, r')
 z2 =  z .* (abs.(z) .< 250)
 contour(r, r, z2)


```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="https://simondanisch.github.io/ReferenceImages/gallery//implicit_equation/media/image.jpg" alt="">

    </p>
</div>

```
