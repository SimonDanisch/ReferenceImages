## Stars

```julia
using Makie

 stars = 100_000
 scene = Scene(backgroundcolor = :black)
 scatter!(
     scene,
     (rand(Point3f0, stars) .- 0.5) .* 10,
     glowwidth = 0.005, glowcolor = :white, color = RGBAf0(0.8, 0.9, 0.95, 0.4),
     markersize = rand(range(0.0001, stop = 0.01, length = 100), stars),
     show_axis = false
 )
 update_cam!(scene, FRect3D(Vec3f0(-2), Vec3f0(4)))
 scene


```
```@raw html

<div style="display:inline-block"><p style="display:inline-block; text-align: center">1<br><img src="/home/sd/ReferenceImages/recordings/stars/media/image.jpg" alt="1<br>">
</p></div>
```
