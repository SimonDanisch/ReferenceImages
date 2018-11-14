## colormaps

```julia
using Makie

 h = 0.0
 offset = 0.1
 scene = Scene()
 cam2d!(scene)
 plot = map(AbstractPlotting.colorbrewer_names) do cmap
     global h
     c = to_colormap(cmap)
     cbar = image!(
         scene,
         range(0, stop = 10, length = length(c)),
         range(0, stop = 1, length = length(c)),
         reshape(c, (1, length(c))),
         show_axis = false
     )[end]
     text!(
         scene,
         string(cmap, ":"),
         position = Point2f0(-0.1, 0.5 + h),
         align = (:right, :center),
         show_axis = false,
         textsize = 0.4
     )
     translate!(cbar, 0, h, 0)
     h -= (1 + offset)
 end
 scene


```
```@raw html

<div style="display:inline-block"><p style="display:inline-block; text-align: center">1<br><img src="/home/sd/ReferenceImages/recordings/colormaps/media/image.jpg" alt="1<br>">
</p></div>
```