## Test

```julia
using AbstractPlotting

 angles = range(0, stop = 2pi, length = 20)
 pos = Point2f0.(sin.(angles), cos.(angles))
 scatter(pos, rotations = -angles , marker = '▲', scale_plot = false)
 scatter!(pos, markersize = 0.02, color = :red, scale_plot = false)


```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="https://simondanisch.github.io/ReferenceImages/gallery//test_14/media/image.jpg" alt="">

    </p>
</div>

```
