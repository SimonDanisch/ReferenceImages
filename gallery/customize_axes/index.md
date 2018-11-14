## Customize Axes

```julia
using Makie

 x = LinRange(0,3pi,200); y = sin.(x)
 lin = lines(x, y, padding = (0.0, 0.0), axis = (
     names = (axisnames = ("", ""),),
     grid = (linewidth = (0, 0),),
 ))


```
```@raw html

<div style="display:inline-block"><p style="display:inline-block; text-align: center">1<br><img src="/home/sd/ReferenceImages/recordings/customize_axes/media/image.jpg" alt="1<br>">
</p></div>
```
