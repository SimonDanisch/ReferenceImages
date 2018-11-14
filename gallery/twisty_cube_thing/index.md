## Twisty cube thing

```julia
using Makie

 (a, b) = -1, 2
 r = range(-2, stop = 2, length = 100)
 z = ((x,y) -> x + y).(r, r') ./ 5
 me = [z .* sin.(3 .* (atan.(y ./ x) .+ z.^2 .+ pi .* (x .> 0))) for x=r, y=r, z=r]
 me2 = me .* (me .> z .* 0.25)
 contour(me2, levels = 6, colormap = :Spectral)


```
```@raw html

<div style="display:inline-block"><p style="display:inline-block; text-align: center">1<br><img src="/home/sd/ReferenceImages/recordings/twisty_cube_thing/media/image.jpg" alt="1<br>">
</p></div>
```
