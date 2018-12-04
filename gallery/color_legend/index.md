## Color Legend

```julia
using AbstractPlotting

 s = surface(0..1, 0..1, rand(100, 100))
 ls = colorlegend(s[end], raw = true, camera = campixel!)
 st = Stepper(vbox(s, ls), "output")
 l = ls[end]
 l[:textcolor] = :blue
 step!(st)
 l[:strokecolor] = :green
 step!(st)
 l[:strokewidth] = 4
 step!(st)
 l[:textsize] = 12
 step!(st)
 l[:textgap] = 5
 step!(st)
 st


```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="https://simondanisch.github.io/ReferenceImages/gallerycolor_legend/media/color_legend-1.jpg" alt="">

    </p>
</div>

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="https://simondanisch.github.io/ReferenceImages/gallerycolor_legend/media/color_legend-2.jpg" alt="">

    </p>
</div>

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="https://simondanisch.github.io/ReferenceImages/gallerycolor_legend/media/color_legend-3.jpg" alt="">

    </p>
</div>

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="https://simondanisch.github.io/ReferenceImages/gallerycolor_legend/media/color_legend-4.jpg" alt="">

    </p>
</div>

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="https://simondanisch.github.io/ReferenceImages/gallerycolor_legend/media/color_legend-5.jpg" alt="">

    </p>
</div>

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="https://simondanisch.github.io/ReferenceImages/gallerycolor_legend/media/thumb.jpg" alt="">

    </p>
</div>

```
