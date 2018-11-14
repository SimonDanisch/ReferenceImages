## 3D Contour with 2D contour slices

```julia
using Makie
 using LinearAlgebra

 function test(x, y, z)
     xy = [x, y, z]
     ((xy') * Matrix(I, 3, 3) * xy) / 20
 end
 x = range(-2pi, stop = 2pi, length = 100)
 scene = Scene()
 c = contour!(scene, x, x, x, test, levels = 6, alpha = 0.3)[end]
 xm, ym, zm = minimum(scene.limits[])
 # c[4] == fourth argument of the above plotting command
 contour!(scene, x, x, map(v-> v[1, :, :], c[4]), transformation = (:xy, zm), linewidth = 10)
 heatmap!(scene, x, x, map(v-> v[:, 1, :], c[4]), transformation = (:xz, ym))
 contour!(scene, x, x, map(v-> v[:, :, 1], c[4]), fillrange = true, transformation = (:yz, xm))


```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="https://raw.githubusercontent.com/SimonDanisch/ReferenceImages/master/gallery/3d_contour_with_2d_contour_slices/media/image.jpg" alt="">

    </p>
</div>

```
