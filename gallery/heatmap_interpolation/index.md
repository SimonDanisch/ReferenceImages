## heatmap interpolation

```julia
using AbstractPlotting
 using AbstractPlotting: hbox, vbox

 data = rand(50, 100)
 p1 = heatmap(data, interpolate = true)
 p2 = heatmap(data, interpolate = false)
 s = vbox(
     title(p1, "interpolate = true";  textsize = 15),
     title(p2, "interpolate = false"; textsize = 15),
 )


```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="https://simondanisch.github.io/ReferenceImages/gallery//heatmap_interpolation/media/image.jpg" alt="">

    </p>
</div>

```
