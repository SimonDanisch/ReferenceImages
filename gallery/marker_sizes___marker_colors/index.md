## Marker sizes + Marker colors

```julia
using Makie

 scatter(
     rand(20), rand(20),
     markersize = rand(20) ./20 .+ 0.02,
     color = rand(RGBf0, 20)
 )


```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="https://raw.githubusercontent.com/SimonDanisch/ReferenceImages/master/gallery/marker_sizes___marker_colors/media/image.jpg" alt="">

    </p>
</div>

```
