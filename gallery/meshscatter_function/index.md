## Meshscatter Function

```julia
using Makie
 using GeometryTypes

 large_sphere = Sphere(Point3f0(0), 1f0)
 positions = decompose(Point3f0, large_sphere)
 colS = [RGBAf0(rand(), rand(), rand(), 1.0) for i = 1:length(positions)]
 sizesS = [rand(Point3f0) .* 0.05f0 for i = 1:length(positions)]
 meshscatter(positions, color = colS, markersize = sizesS)


```
```@raw html

<div style="display:inline-block"><p style="display:inline-block; text-align: center">1<br><img src="/home/sd/ReferenceImages/recordings/meshscatter_function/media/image.jpg" alt="1<br>">
</p></div>
```
