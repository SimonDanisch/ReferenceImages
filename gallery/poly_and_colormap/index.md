## poly and colormap

```julia
using AbstractPlotting

 points = Point2f0[[0.0, 0.0], [0.1, 0.0], [0.1, 0.1], [0.0, 0.1]]
 colors = [0.0 ,0.0, 0.5, 0.0]
 scene = poly(points, color = colors, colorrange = (0.0,1.0))
 points = Point2f0[[0.1, 0.1], [0.2, 0.1], [0.2, 0.2], [0.1, 0.2]]
 colors = [0.5,0.5,1.0,0.3]
 poly!(scene, points, color = colors, colorrange = (0.0,1.0))
 scene


```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="https://simondanisch.github.io/ReferenceImages/gallery//poly_and_colormap/media/image.jpg" alt="">

    </p>
</div>

```
