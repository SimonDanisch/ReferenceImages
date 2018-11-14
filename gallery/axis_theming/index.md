## Axis theming

```julia
using Makie
 using GeometryTypes

 scene = Scene()
 points = decompose(Point2f0, Circle(Point2f0(10), 10f0), 9)
 lines!(
     scene,
     points,
     linewidth = 8,
     color = :black
 )

 axis = scene[Axis] # get axis
 scene

 st = Stepper(scene, "output")
 step!(st);
 axis[:frame][:linewidth] = 5
 step!(st)
 axis[:grid][:linewidth] = (1, 5)
 step!(st)
 axis[:grid][:linecolor] = ((:red, 0.3), (:blue, 0.5))
 step!(st)
 axis[:names][:axisnames] = ("x", "y   ")
 step!(st)
 axis[:ticks][:title_gap] = 1
 step!(st)
 axis[:names][:rotation] = (0.0, -3/8*pi)
 step!(st)
 axis[:names][:textcolor] = ((:red, 1.0), (:blue, 1.0))
 step!(st)
 axis[:ticks][:font] = ("Dejavu Sans", "Helvetica")
 step!(st)
 axis[:ticks][:rotation] = (0.0, -pi/2)
 step!(st)
 axis[:ticks][:textsize] = (3, 7)
 step!(st)
 axis[:ticks][:gap] = 5
 step!(st)


```
```@raw html

<div style="display:inline-block"><p style="display:inline-block; text-align: center">1<br><img src="/home/sd/ReferenceImages/recordings/axis_theming/media/axis_theming-1.jpg" alt="1<br>">
</p></div>
<div style="display:inline-block"><p style="display:inline-block; text-align: center">2<br><img src="/home/sd/ReferenceImages/recordings/axis_theming/media/axis_theming-10.jpg" alt="2<br>">
</p></div>
<div style="display:inline-block"><p style="display:inline-block; text-align: center">3<br><img src="/home/sd/ReferenceImages/recordings/axis_theming/media/axis_theming-11.jpg" alt="3<br>">
</p></div>
<div style="display:inline-block"><p style="display:inline-block; text-align: center">4<br><img src="/home/sd/ReferenceImages/recordings/axis_theming/media/axis_theming-12.jpg" alt="4<br>">
</p></div>
<div style="display:inline-block"><p style="display:inline-block; text-align: center">5<br><img src="/home/sd/ReferenceImages/recordings/axis_theming/media/axis_theming-2.jpg" alt="5<br>">
</p></div>
<div style="display:inline-block"><p style="display:inline-block; text-align: center">6<br><img src="/home/sd/ReferenceImages/recordings/axis_theming/media/axis_theming-3.jpg" alt="6<br>">
</p></div>
<div style="display:inline-block"><p style="display:inline-block; text-align: center">7<br><img src="/home/sd/ReferenceImages/recordings/axis_theming/media/axis_theming-4.jpg" alt="7<br>">
</p></div>
<div style="display:inline-block"><p style="display:inline-block; text-align: center">8<br><img src="/home/sd/ReferenceImages/recordings/axis_theming/media/axis_theming-5.jpg" alt="8<br>">
</p></div>
<div style="display:inline-block"><p style="display:inline-block; text-align: center">9<br><img src="/home/sd/ReferenceImages/recordings/axis_theming/media/axis_theming-6.jpg" alt="9<br>">
</p></div>
<div style="display:inline-block"><p style="display:inline-block; text-align: center">10<br><img src="/home/sd/ReferenceImages/recordings/axis_theming/media/axis_theming-7.jpg" alt="10<br>">
</p></div>
<div style="display:inline-block"><p style="display:inline-block; text-align: center">11<br><img src="/home/sd/ReferenceImages/recordings/axis_theming/media/axis_theming-8.jpg" alt="11<br>">
</p></div>
<div style="display:inline-block"><p style="display:inline-block; text-align: center">12<br><img src="/home/sd/ReferenceImages/recordings/axis_theming/media/axis_theming-9.jpg" alt="12<br>">
</p></div>
```
