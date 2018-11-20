## Unicode Marker

```julia
using Makie

 scene = Scene(resolution = (500, 500))
 scatter!(scene, Point3f0[(1,0,0), (0,1,0), (0,0,1)], marker = [:x, :circle, :cross])


```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="/home/sd/.julia/dev/MakieGallery/test/test_recordings/unicode_marker/media/image.jpg" alt="">

    </p>
</div>

```
