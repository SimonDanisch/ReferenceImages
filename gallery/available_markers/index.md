## Available markers

```julia
using AbstractPlotting

 marker = collect(AbstractPlotting._marker_map)
 positions = Point2f0.(0, 1:length(marker))
 scene = scatter(
     positions,
     marker = last.(marker),
     markersize = 0.8,
     marker_offset = Vec2f0(0.5, -0.4),
     show_axis = false,
 )
 annotations!(
     scene,
     string.(":", first.(marker)),
     positions,
     align = (:right, :center),
     textsize = 0.4,
     raw = true
 )
 update_cam!(scene, FRect(-2.5, 0, 2, length(marker) + 2))
 scene


```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="https://simondanisch.github.io/ReferenceImages/gallery//available_markers/media/image.jpg" alt="">

    </p>
</div>

```
