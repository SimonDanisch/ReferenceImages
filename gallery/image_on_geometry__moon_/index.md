## Image on Geometry (Moon)

```julia
using AbstractPlotting, GLMakie, GLMakie
 using FileIO

 moon = try
     load(download("https://svs.gsfc.nasa.gov/vis/a000000/a004600/a004675/phases.0001_print.jpg"))
 catch e
     @warn("Download the moon failed. Using random image, so this test will fail! (error: $e)")
     rand(RGBAf0, 100, 100) # don't error test when e.g. offline
 end
 scene = mesh(Sphere(Point3f0(0), 1f0), color = moon, shading = false, show_axis = false, center = false)
 update_cam!(scene, Vec3f0(-2, 2, 2), Vec3f0(0))
 scene.center = false # prevent to recenter on display
 scene


```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="https://simondanisch.github.io/ReferenceImages/gallery//image_on_geometry__moon_/media/image.jpg" alt="">

    </p>
</div>

```
