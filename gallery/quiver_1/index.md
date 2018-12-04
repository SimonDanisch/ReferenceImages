## quiver

```julia
using AbstractPlotting
 using ImageFiltering

 x = range(-2, stop = 2, length = 21)
 y = x
 z = x .* exp.(-x .^ 2 .- (y') .^ 2)
 scene = contour(x, y, z, levels = 10, linewidth = 3)
 u, v = ImageFiltering.imgradients(z, KernelFactors.ando3)
 arrows!(x, y, u, v, arrowsize = 0.05)


```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="https://simondanisch.github.io/ReferenceImages/galleryquiver_1/media/image.jpg" alt="">

    </p>
</div>

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="https://simondanisch.github.io/ReferenceImages/galleryquiver_1/media/thumb.jpg" alt="">

    </p>
</div>

```
