## Test

```julia
using AbstractPlotting

contour(rand(33, 30) .* 6 .- 3, levels=[-2.5, 0.4, 0.5, 0.6, 2.5], colormap=[(:black, 0.2), :red, :blue, :green, (:black, 0.2)], colorrange=(0.2, 0.8))

```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="https://simondanisch.github.io/ReferenceImages/gallery//test_30/media/image.jpg" alt="">

    </p>
</div>

```
