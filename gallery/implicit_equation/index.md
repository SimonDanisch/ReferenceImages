## Implicit equation

```julia
using Makie

 r = range(-5, stop = 5, length = 400)
 (a, b) = -1, 2
 z = ((x,y) -> y.^4 - x.^4 + a .* y.^2 + b .* x.^2).(r, r')
 z2 =  z .* (abs.(z) .< 250)
 contour(r, r, z2)


```
```@raw html

<div style="display:inline-block"><p style="display:inline-block; text-align: center">1<br><img src="/home/sd/ReferenceImages/recordings/implicit_equation/media/image.jpg" alt="1<br>">
</p></div>
```
