## Test

```julia
using AbstractPlotting

 scene = Scene()
 cam2d!(scene)
 axis2d!(
     scene, IRect(Vec2f0(0), Vec2f0(1)),
     ticks = (
         ranges = ([0.1, 0.2, 0.9], [0.1, 0.2, 0.9]),
         labels = (["😸", "♡", "𝕴"], ["β ÷ δ", "22", "≙"])
     ), raw = true
 )
 center!(scene)
 scene


```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="https://simondanisch.github.io/ReferenceImages/gallery//test_13/media/image.jpg" alt="">

    </p>
</div>

```
