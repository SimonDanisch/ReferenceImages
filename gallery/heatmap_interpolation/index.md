## heatmap interpolation

```julia
using Makie
 using AbstractPlotting: hbox, vbox

 data = rand(50, 100)
 p1 = heatmap(data, interpolate = true)
 p2 = heatmap(data, interpolate = false)
 t = Theme(align = (:left, :bottom), raw = true, camera = campixel!)
 title1 = text(t, "Interpolate = true")
 title2 = text(t, "Interpolate = false")
 s = vbox(
     hbox(p1, title1),
     hbox(p2, title2),
 )


```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="https://raw.githubusercontent.com/SimonDanisch/ReferenceImages/master/gallery/heatmap_interpolation/media/image.jpg" alt="">

    </p>
</div>

```
