## Meshscatter Function

```julia
using AbstractPlotting
 using GeometryTypes

 large_sphere = Sphere(Point3f0(0), 1f0)
 positions = decompose(Point3f0, large_sphere)
 colS = [RGBAf0(rand(), rand(), rand(), 1.0) for i = 1:length(positions)]
 sizesS = [rand(Point3f0) .* 0.05f0 for i = 1:length(positions)]
 meshscatter(positions, color = colS, markersize = sizesS)


```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="https://simondanisch.github.io/ReferenceImages/gallery//meshscatter_function/media/image.jpg" alt="">

    </p>
</div>

```
