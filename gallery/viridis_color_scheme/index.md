## Viridis color scheme

```julia
using AbstractPlotting

 c = to_colormap(:viridis) # get colors of colormap

 image(         # to plot colors, an image is best
    0..10,      # x range
    0..1,       # y range
    hcat(c, c), # reshape this to a matrix for the colors
    show_axis = false # don't show axes
 )



```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="https://simondanisch.github.io/ReferenceImages/gallery//viridis_color_scheme/media/image.jpg" alt="">

    </p>
</div>

```
