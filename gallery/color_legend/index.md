## Color Legend

```julia
using Makie
 using Makie

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

<div style="display:inline-block"><p style="display:inline-block; text-align: center">1<br><img src="/home/sd/ReferenceImages/recordings/color_legend/media/color_legend-1.jpg" alt="1<br>">
</p></div>
<div style="display:inline-block"><p style="display:inline-block; text-align: center">2<br><img src="/home/sd/ReferenceImages/recordings/color_legend/media/color_legend-2.jpg" alt="2<br>">
</p></div>
<div style="display:inline-block"><p style="display:inline-block; text-align: center">3<br><img src="/home/sd/ReferenceImages/recordings/color_legend/media/color_legend-3.jpg" alt="3<br>">
</p></div>
<div style="display:inline-block"><p style="display:inline-block; text-align: center">4<br><img src="/home/sd/ReferenceImages/recordings/color_legend/media/color_legend-4.jpg" alt="4<br>">
</p></div>
<div style="display:inline-block"><p style="display:inline-block; text-align: center">5<br><img src="/home/sd/ReferenceImages/recordings/color_legend/media/color_legend-5.jpg" alt="5<br>">
</p></div>
```
