## Polygons

```julia
using Makie
 using GeometryTypes

 scene = Scene(resolution = (500, 500))
 points = decompose(Point2f0, Circle(Point2f0(50), 50f0))
 pol = poly!(scene, points, color = :gray, strokewidth = 10, strokecolor = :red)
 # Optimized forms
 poly!(scene, [Circle(Point2f0(50+300), 50f0)], color = :gray, strokewidth = 10, strokecolor = :red)
 poly!(scene, [Circle(Point2f0(50+i, 50+i), 10f0) for i = 1:100:400], color = :red)
 poly!(scene, [Rectangle{Float32}(50+i, 50+i, 20, 20) for i = 1:100:400], strokewidth = 2, strokecolor = :green)
 linesegments!(scene,
     [Point2f0(50 + i, 50 + i) => Point2f0(i + 70, i + 70) for i = 1:100:400], linewidth = 8, color = :purple
 )


```
```@raw html

<div style="display:inline-block"><p style="display:inline-block; text-align: center">1<br><img src="/home/sd/ReferenceImages/recordings/polygons/media/image.jpg" alt="1<br>">
</p></div>
```
