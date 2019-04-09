## Test

```julia
using AbstractPlotting

contour(rand(33, 30) .* 6 .- 3, levels=[-2.5, 0.4, 0.5, 0.6, 2.5], colormap=[(:black, 0.2), :red, :blue, :green, (:black, 0.2)], colorrange=(0.2, 0.8))

```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="https://simondanisch.github.io/ReferenceImages/gallery//test_1_2_3_4_5_6_7_8_9_10_11_12_13_14_15_16_17_18_19_20_21_22_23_24_25_26_27_28_29_30/media/image.jpg" alt="">

    </p>
</div>

```
