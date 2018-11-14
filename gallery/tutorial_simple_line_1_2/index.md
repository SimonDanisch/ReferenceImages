## Tutorial simple line

```julia
using Makie

 x = range(0, stop = 2pi, length = 40)
 f(x) = sin.(x)
 y = f(x)

 scene = lines(x, y, color = :blue)


```
```@raw html

<div style="display:inline-block"><p style="display:inline-block; text-align: center">1<br><img src="/home/sd/ReferenceImages/recordings/tutorial_simple_line_1_2/media/image.jpg" alt="1<br>">
</p></div>
```
