## Line Function

```julia
using Makie

 scene = Scene()
 x = range(0, stop = 3pi)
 lines!(scene, x, sin.(x))
 lines!(scene, x, cos.(x), color = :blue)


```
```@raw html

<div style="display:inline-block"><p style="display:inline-block; text-align: center">1<br><img src="/home/sd/ReferenceImages/recordings/line_function/media/image.jpg" alt="1<br>">
</p></div>
```
