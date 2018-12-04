## Contour Function

```julia
using AbstractPlotting

 r = range(-10, stop = 10, length = 512)
 z = ((x, y)-> sin(x) + cos(y)).(r, r')
 contour(r, r, z, levels = 5, color = :viridis, linewidth = 3)


```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="https://simondanisch.github.io/ReferenceImages/gallerycontour_function/media/image.jpg" alt="">

    </p>
</div>

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="https://simondanisch.github.io/ReferenceImages/gallerycontour_function/media/thumb.jpg" alt="">

    </p>
</div>

```
