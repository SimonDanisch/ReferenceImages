## Test

```julia
using AbstractPlotting

 r = range(-3pi, stop = 3pi, length = 100)
 s = volume(r, r, r, (x, y, z)-> cos(x) + sin(y) + cos(z), algorithm = :iso, isorange = 0.1f0, show_axis = false)
 v2 = volume!(r, r, r, (x, y, z)-> cos(x) + sin(y) + cos(z), algorithm = :mip, show_axis = false)[end]
 translate!(v2, Vec3f0(6pi, 0, 0))
 s


```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="https://simondanisch.github.io/ReferenceImages/gallery//test_1/media/image.jpg" alt="">

    </p>
</div>

```
