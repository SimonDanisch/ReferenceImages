## Cube lattice

```julia
using Makie

 r = range(-3, stop = 3, length = 100)
 me = [((1 ./ x).^2 + (1 ./ y).^2 + (1 ./ z).^2) for x=r, y=r, z=r]
 me2 = me .* (abs.(me) .> 1.5)
 contour(me2, color = :Set2)


```
```@raw html

<div style="display:inline-block"><p style="display:inline-block; text-align: center">1<br><img src="/home/sd/ReferenceImages/recordings/cube_lattice/media/image.jpg" alt="1<br>">
</p></div>
```
