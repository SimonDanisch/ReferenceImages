## image scatter

```julia
using AbstractPlotting
 using LinearAlgebra

 scatter(
     1:10, 1:10, rand(10, 10) .* 10,
     rotations = normalize.(rand(Quaternionf0, 10*10)),
     markersize = 1,
     # can also be an array of images for each point
     # need to be the same size for best performance, though
     marker = AbstractPlotting.logo()
 )


```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="https://simondanisch.github.io/ReferenceImages/galleryimage_scatter/media/image.jpg" alt="">

    </p>
</div>

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="https://simondanisch.github.io/ReferenceImages/galleryimage_scatter/media/thumb.jpg" alt="">

    </p>
</div>

```
