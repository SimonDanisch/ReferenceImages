## Surface

```julia
using Makie

 N = 30
 function xy_data(x, y)
     r = sqrt(x^2 + y^2)
     r == 0.0 ? 1f0 : (sin(r)/r)
 end
 lspace = range(-10, stop = 10, length = N)
 z = Float32[xy_data(x, y) for x in lspace, y in lspace]
 r = range(0, stop = 3, length = N)
 surface(
     r, r, z,
     colormap = :Spectral
 )


```
```@raw html

<div style="display:inline-block"><p style="display:inline-block; text-align: center">1<br><img src="/home/sd/ReferenceImages/recordings/surface_1_2/media/image.jpg" alt="1<br>">
</p></div>
```
