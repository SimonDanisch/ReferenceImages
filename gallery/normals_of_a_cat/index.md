## Normals of a Cat

```julia
using AbstractPlotting
 using LinearAlgebra, GLMakie

 x = GLMakie.loadasset("cat.obj")
 mesh(x, color = :black)
 pos = map(x.vertices, x.normals) do p, n
     p => p .+ (normalize(n) .* 0.05f0)
 end
 linesegments!(pos, color = :blue)


```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="https://simondanisch.github.io/ReferenceImages/gallerynormals_of_a_cat/media/image.jpg" alt="">

    </p>
</div>

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="https://simondanisch.github.io/ReferenceImages/gallerynormals_of_a_cat/media/thumb.jpg" alt="">

    </p>
</div>

```
