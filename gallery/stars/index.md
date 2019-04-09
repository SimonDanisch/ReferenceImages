## Stars

```julia
using AbstractPlotting

 stars = 100_000
 scene = Scene(backgroundcolor = :black)
 scatter!(
     scene,
     (randn(Point3f0, stars) .- 0.5) .* 10,
     glowwidth = 1, glowcolor = (:white, 0.1), color = rand(stars),
     colormap = [(:white, 0.4), (:blue, 0.4), (:yellow, 0.4)],
     markersize = rand(range(0.0001, stop = 0.05, length = 100), stars),
     show_axis = false, transparency = true
 )
 update_cam!(scene, FRect3D(Vec3f0(-5), Vec3f0(10)))
 scene.center = false
 scene


```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="https://simondanisch.github.io/ReferenceImages/gallery//stars/media/image.jpg" alt="">

    </p>
</div>

```
