## Surface + wireframe + contour

```julia
using Makie

 N = 51
 x = range(-2, stop = 2, length = N)
 y = x
 z = (-x .* exp.(-x .^ 2 .- (y') .^ 2)) .* 4

 scene = wireframe(x, y, z)
 xm, ym, zm = minimum(scene.limits[])
 scene = surface!(scene, x, y, z .+ 0.05)
 contour!(scene, x, y, z, levels = 15, linewidth = 2, transformation = (:xy, zm))
 scene


```
```@raw html

<div style="display:inline-block"><p style="display:inline-block; text-align: center">1<br><img src="/home/sd/ReferenceImages/recordings/surface___wireframe___contour_1_2/media/image.jpg" alt="1<br>">
</p></div>
```
