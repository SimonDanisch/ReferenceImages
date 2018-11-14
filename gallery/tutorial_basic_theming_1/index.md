## Tutorial basic theming

```julia
using Makie

 x = range(0, stop = 2pi, length = 40)
 f(x) = cos.(x)
 y = f(x)
 scene = lines(x, y, color = :blue)

 axis = scene[Axis] # get the axis object from the scene
 axis[:grid][:linecolor] = ((:red, 0.5), (:blue, 0.5))
 axis[:names][:textcolor] = ((:red, 1.0), (:blue, 1.0))
 axis[:names][:axisnames] = ("x", "y = cos(x)")
 scene


```
```@raw html

<div style="display:inline-block"><p style="display:inline-block; text-align: center">1<br><img src="/home/sd/ReferenceImages/recordings/tutorial_basic_theming_1/media/image.jpg" alt="1<br>">
</p></div>
```
