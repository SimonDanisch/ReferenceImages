## surface + contour3d

```julia
using Makie

 vx = -1:0.01:1
 vy = -1:0.01:1

 f(x, y) = (sin(x*10) + cos(y*10)) / 4

 p1 = surface(vx, vy, f)
 p2 = contour3d(vx, vy, (x, y) -> f(x,y), levels = 15, linewidth = 3)

 scene = vbox(p1, p2)
 text!(campixel(p1), "surface", position = widths(p1) .* Vec(0.5, 1), align = (:center, :top), raw = true)
 text!(campixel(p2), "contour3d", position = widths(p2) .* Vec(0.5, 1), align = (:center, :top), raw = true)
 scene


```
```@raw html

<div style="display:inline-block"><p style="display:inline-block; text-align: center">1<br><img src="/home/sd/ReferenceImages/recordings/surface___contour3d_1_2/media/image.jpg" alt="1<br>">
</p></div>
```
