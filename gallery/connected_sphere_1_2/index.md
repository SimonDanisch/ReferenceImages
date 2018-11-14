## Connected Sphere

```julia
using Makie

 large_sphere = Sphere(Point3f0(0), 1f0)
 positions = decompose(Point3f0, large_sphere)
 linepos = view(positions, rand(1:length(positions), 1000))
 scene = lines(linepos, linewidth = 0.1, color = :black)
 scatter!(scene, positions, strokewidth = 10, strokecolor = :white, color = RGBAf0(0.9, 0.2, 0.4, 0.6))
 scene


```
```@raw html

<div style="display:inline-block"><p style="display:inline-block; text-align: center">1<br><img src="/home/sd/ReferenceImages/recordings/connected_sphere_1_2/media/image.jpg" alt="1<br>">
</p></div>
```
