## Test

```julia
using Makie

 angles = range(0, stop = 2pi, length = 20)
 pos = Point2f0.(sin.(angles), cos.(angles))
 scatter(pos, rotations = -angles , marker = '▲', scale_plot = false)
 scatter!(pos, markersize = 0.02, color = :red, scale_plot = false)


```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="https://raw.githubusercontent.com/SimonDanisch/ReferenceImages/master/gallery/test_1_2_3_4_5_6_7_8_9_10_11/media/image.jpg" alt="">

    </p>
</div>

```
