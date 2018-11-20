## 3D cube with sphere cutout, outside

```julia
using Makie

 scene = Scene()
 r = range(-1, stop = 1, length = 100)
 mat = [(x.^2 + y.^2 + z.^2) for x=r, y=r, z=r]
 mat2 = mat .* (mat .< 1.4)
 #plot the space outside
 volume(50..100, 50..100, 50..100, mat2, algorithm = :absorptionrgba)


```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="/home/sd/.julia/dev/MakieGallery/test/test_recordings/3d_cube_with_sphere_cutout,_outside/media/image.jpg" alt="">

    </p>
</div>

```
