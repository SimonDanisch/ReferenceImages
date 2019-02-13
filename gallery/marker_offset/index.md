## Marker offset

```julia
using AbstractPlotting

 scene = Scene(resolution = (500, 500))
 points = Point2f0[(0,0), (1,1), (2,2)]
 offset = rand(Point2f0, 3)./5
 scatter!(scene, points)
 scatter!(scene, points, marker_offset = offset, color = :red)


```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="https://simondanisch.github.io/ReferenceImages/gallery/\\marker_offset\\media\\image.jpg" alt="">

    </p>
</div>

```
