## Available markers

```julia
using AbstractPlotting
 using GeometryTypes

 scene = Scene()
 cam2d!(scene)
 marker = collect(AbstractPlotting._marker_map)
 positions = Point2f0.(0, 1:length(marker))
 scatter!(
     scene,
     positions,
     marker = last.(marker),
     markersize = 0.8,
     raw = true,
     marker_offset = Vec2f0(0.5, -0.4)
 )
 annotations!(
     scene,
     string.(":", first.(marker)),
     positions,
     align = (:right, :center),
     textsize = 0.4,
     raw = true
 )


```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="https://simondanisch.github.io/ReferenceImages/gallery/\\available_markers\\media\\image.jpg" alt="">

    </p>
</div>

```
