## Wireframe of a Surface

```julia
using AbstractPlotting

 function xy_data(x, y)
     r = sqrt(x^2 + y^2)
     r == 0.0 ? 1f0 : (sin(r)/r)
 end
 N = 30
 lspace = range(-10, stop = 10, length = N)
 z = Float32[xy_data(x, y) for x in lspace, y in lspace]
 r = range(0, stop = 3, length = N)
 wireframe(r, r, z)


```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="https://simondanisch.github.io/ReferenceImages/gallery/\\wireframe_of_a_surface\\media\\image.jpg" alt="">

    </p>
</div>

```
