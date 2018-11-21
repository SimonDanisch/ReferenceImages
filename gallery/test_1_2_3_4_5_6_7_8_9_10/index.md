## Test

```julia
using Makie

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
        <img src="https://raw.githubusercontent.com/SimonDanisch/ReferenceImages/master/gallery/test_1_2_3_4_5_6_7_8_9_10/media/image.jpg" alt="">

    </p>
</div>

```
