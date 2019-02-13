## FEM polygon 2D

```julia
using AbstractPlotting

 coordinates = [
     0.0 0.0;
     0.5 0.0;
     1.0 0.0;
     0.0 0.5;
     0.5 0.5;
     1.0 0.5;
     0.0 1.0;
     0.5 1.0;
     1.0 1.0;
 ]
 connectivity = [
     1 2 5;
     1 4 5;
     2 3 6;
     2 5 6;
     4 5 8;
     4 7 8;
     5 6 9;
     5 8 9;
 ]
 color = [0.0, 0.0, 0.0, 0.0, -0.375, 0.0, 0.0, 0.0, 0.0]
 poly(coordinates, connectivity, color = color, strokecolor = (:black, 0.6), strokewidth = 4)


```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="https://simondanisch.github.io/ReferenceImages/gallery/\\fem_polygon_2d\\media\\image.jpg" alt="">

    </p>
</div>

```
