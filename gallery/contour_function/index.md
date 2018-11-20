## Contour Function

```julia
using Makie

 r = range(-10, stop = 10, length = 512)
 z = ((x, y)-> sin(x) + cos(y)).(r, r')
 contour(r, r, z, levels = 5, color = :viridis, linewidth = 3)


```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="/home/sd/.julia/dev/MakieGallery/test/test_recordings/contour_function/media/image.jpg" alt="">

    </p>
</div>

```
