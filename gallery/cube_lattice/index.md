## Cube lattice

```julia
using AbstractPlotting, GLMakie, GLMakie

 r = range(-3, stop = 3, length = 100)
 me = [((1 ./ x).^2 + (1 ./ y).^2 + (1 ./ z).^2) for x=r, y=r, z=r]
 me2 = me .* (abs.(me) .> 1.5)
 contour(me2, colormap = :Set2)


```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="https://simondanisch.github.io/ReferenceImages/gallery//cube_lattice/media/image.jpg" alt="">

    </p>
</div>

```
