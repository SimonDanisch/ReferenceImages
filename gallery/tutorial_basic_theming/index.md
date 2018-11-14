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

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="https://raw.githubusercontent.com/SimonDanisch/ReferenceImages/master/gallery/tutorial_basic_theming/media/image.jpg" alt="">

    </p>
</div>

```
