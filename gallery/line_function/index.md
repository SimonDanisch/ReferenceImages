## Line Function

```julia
using AbstractPlotting, GLMakie, GLMakie

 scene = Scene()
 x = range(0, stop = 3pi)
 lines!(scene, x, sin.(x))
 lines!(scene, x, cos.(x), color = :blue)


```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="https://simondanisch.github.io/ReferenceImages/gallery//line_function/media/image.jpg" alt="">

    </p>
</div>

```
