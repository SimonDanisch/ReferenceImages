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

<div style="display:inline-block"><p style="display:inline-block; text-align: center">1<br><img src="/home/sd/ReferenceImages/recordings/heatmap_interpolation_1_2/media/image.jpg" alt="1<br>">
</p></div>
```
