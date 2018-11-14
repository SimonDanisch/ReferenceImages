## Normals of a Cat

```julia
using Makie
 using LinearAlgebra

 x = Makie.loadasset("cat.obj")
 mesh(x, color = :black)
 pos = map(x.vertices, x.normals) do p, n
     p => p .+ (normalize(n) .* 0.05f0)
 end
 linesegments!(pos, color = :blue)


```
```@raw html

<div style="display:inline-block"><p style="display:inline-block; text-align: center">1<br><img src="/home/sd/ReferenceImages/recordings/normals_of_a_cat_1/media/image.jpg" alt="1<br>">
</p></div>
```
