## Test heatmap + image overlap

```julia
using AbstractPlotting

 heatmap(rand(32, 32))
 image!(map(x->RGBAf0(x,0.5, 0.5, 0.8), rand(32,32)))


```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="https://simondanisch.github.io/ReferenceImages/gallerytest_heatmap___image_overlap/media/image.jpg" alt="">

    </p>
</div>

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="https://simondanisch.github.io/ReferenceImages/gallerytest_heatmap___image_overlap/media/thumb.jpg" alt="">

    </p>
</div>

```
