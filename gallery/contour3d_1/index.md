## Contour3d

```julia
using Makie

 function xy_data(x, y)
     r = sqrt(x*x + y*y)
     r == 0.0 ? 1f0 : (sin(r)/r)
 end
 r = range(-1, stop = 1, length = 100)
 contour3d(r, r, (x,y)-> xy_data(10x, 10y), levels = 20, linewidth = 3)


```
```@raw html

<div style="display:inline-block"><p style="display:inline-block; text-align: center">1<br><img src="/home/sd/ReferenceImages/recordings/contour3d_1/media/image.jpg" alt="1<br>">
</p></div>
```
