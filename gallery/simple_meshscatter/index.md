## Simple meshscatter

```julia
using Makie

 large_sphere = Sphere(Point3f0(0), 1f0)
 positions = decompose(Point3f0, large_sphere)
 meshscatter(positions, color = RGBAf0(0.9, 0.2, 0.4, 1), markersize = 0.05)


```
```@raw html

<div style="display:inline-block"><p style="display:inline-block; text-align: center">1<br><img src="/home/sd/ReferenceImages/recordings/simple_meshscatter/media/image.jpg" alt="1<br>">
</p></div>
```
