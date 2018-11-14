## quiver

```julia
using Makie
 using ImageFiltering

 x = range(-2, stop = 2, length = 21)
 y = x
 z = x .* exp.(-x .^ 2 .- (y') .^ 2)
 scene = contour(x, y, z, levels = 10, linewidth = 3)
 u, v = ImageFiltering.imgradients(z, KernelFactors.ando3)
 arrows!(x, y, u, v, arrowsize = 0.05)


```
```@raw html

<div style="display:inline-block"><p style="display:inline-block; text-align: center">1<br><img src="/home/sd/ReferenceImages/recordings/quiver_1_2_3/media/image.jpg" alt="1<br>">
</p></div>
```
