## Test heatmap + image overlap

```julia
using Makie

 heatmap(rand(32, 32))
 image!(map(x->RGBAf0(x,0.5, 0.5, 0.8), rand(32,32)))


```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="/home/sd/.julia/dev/MakieGallery/test/test_recordings/test_heatmap___image_overlap/media/image.jpg" alt="">

    </p>
</div>

```
