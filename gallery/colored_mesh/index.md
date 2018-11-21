## Colored Mesh

```julia
using Makie

 x = [0, 1, 2, 0]
 y = [0, 0, 1, 2]
 z = [0, 2, 0, 1]
 color = [:red, :green, :blue, :yellow]
 i = [0, 0, 0, 1]
 j = [1, 2, 3, 2]
 k = [2, 3, 1, 3]
 # indices interpreted as triangles (every 3 sequential indices)
 indices = [1, 2, 3,   1, 3, 4,   1, 4, 2,   2, 3, 4]
 mesh(x, y, z, indices, color = color)


```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="https://raw.githubusercontent.com/SimonDanisch/ReferenceImages/master/gallery/colored_mesh/media/image.jpg" alt="">

    </p>
</div>

```
