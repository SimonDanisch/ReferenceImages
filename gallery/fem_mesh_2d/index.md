## FEM mesh 2D

```julia
using Makie

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
 scene = mesh(coordinates, connectivity, color = color, shading = false)
 wireframe!(scene[end][1], color = (:black, 0.6), linewidth = 3)


```
```@raw html

<div style="display:inline-block"><p style="display:inline-block; text-align: center">1<br><img src="/home/sd/ReferenceImages/recordings/fem_mesh_2d/media/image.jpg" alt="1<br>">
</p></div>
```
