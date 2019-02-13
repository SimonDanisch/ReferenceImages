## 3D cube with sphere cutout, inside

```julia
using AbstractPlotting

 scene = Scene()
 r = range(-1, stop = 1, length = 100)
 mat = [(x.^2 + y.^2 + z.^2) for x = r, y = r, z = r]
 mat2 = mat .* (mat .> 1.4)
 #plot the space inside
 volume(mat2, algorithm = :absorptionrgba)


```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="https://simondanisch.github.io/ReferenceImages/gallery/\\3d_cube_with_sphere_cutout,_inside\\media\\image.jpg" alt="">

    </p>
</div>

```
