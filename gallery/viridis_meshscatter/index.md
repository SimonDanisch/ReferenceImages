## Viridis meshscatter

```julia
using Makie

 N = 30
 R = 2
 theta = 4pi
 h = 5
 x = [R .* (t/3) .* cos(t) for t = range(0, stop = theta, length = N)]
 y = [R .* (t/3) .* sin(t) for t = range(0, stop = theta, length = N)]
 z = range(0, stop = h, length = N)
 meshscatter(x, y, z, markersize = 0.5, color = to_colormap(:viridis, N))


```
```@raw html

<div style="display:inline-block"><p style="display:inline-block; text-align: center">1<br><img src="/home/sd/ReferenceImages/recordings/viridis_meshscatter/media/image.jpg" alt="1<br>">
</p></div>
```
