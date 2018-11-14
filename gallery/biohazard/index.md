## Biohazard

```julia
using Makie

 (a, b) = -1, 2
 r = range(-5, stop = 5, length = 100)
 z = ((x,y) -> y.^4 - x.^4 + a.*y.^2 + b.*x.^2).(r, r')
 me = [cos.(2 .* pi .* sqrt.(x.^2 + y.^2)) .* (4 .* z) for x=r, y=r, z=r]
 me2 = me .* (abs.(me) .> z .* 3)
 volume(me2, algorithm = :absorptionrgba)


```
```@raw html

<div style="display:inline-block"><p style="display:inline-block; text-align: center">1<br><img src="/home/sd/ReferenceImages/recordings/biohazard/media/image.jpg" alt="1<br>">
</p></div>
```
