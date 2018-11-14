## Marker offset

```julia
using Makie

 scene = Scene(resolution = (500, 500))
 points = Point2f0[(0,0), (1,1), (2,2)]
 offset = rand(Point2f0, 3)./5
 scatter!(scene, points)
 scatter!(scene, points, marker_offset = offset, color = :red)


```
```@raw html

<div style="display:inline-block"><p style="display:inline-block; text-align: center">1<br><img src="/home/sd/ReferenceImages/recordings/marker_offset/media/image.jpg" alt="1<br>">
</p></div>
```
