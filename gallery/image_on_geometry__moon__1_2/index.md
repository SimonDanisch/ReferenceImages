## Image on Geometry (Moon)

```julia
using Makie
 using FileIO

 moon = try
     load(download("https://svs.gsfc.nasa.gov/vis/a000000/a004600/a004675/phases.0001_print.jpg"))
 catch e
     @warn("Download the moon failed. Using random image, so this test will fail! (error: $e)")
     rand(RGBAf0, 100, 100) # don't error test when e.g. offline
 end
 scene = mesh(Sphere(Point3f0(0), 1f0), color = moon, shading = false, show_axis = false, center = false)
 update_cam!(scene, Vec3f0(-2, 2, 2), Vec3f0(0))
 scene


```
```@raw html

<div style="display:inline-block"><p style="display:inline-block; text-align: center">1<br><img src="/home/sd/ReferenceImages/recordings/image_on_geometry__moon__1_2/media/image.jpg" alt="1<br>">
</p></div>
```
