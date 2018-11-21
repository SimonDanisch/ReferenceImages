## Surface with image

```julia
using Makie

 N = 30
 function xy_data(x, y)
     r = sqrt(x^2 + y^2)
     r == 0.0 ? 1f0 : (sin(r)/r)
 end
 r = range(-2, stop = 2, length = N)
 surf_func(i) = [Float32(xy_data(x*i, y*i)) for x = r, y = r]
 surface(
     r, r, surf_func(10),
     color = rand(RGBAf0, 124, 124)
 )


```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="https://raw.githubusercontent.com/SimonDanisch/ReferenceImages/master/gallery/surface_with_image/media/image.jpg" alt="">

    </p>
</div>

```
