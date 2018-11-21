## Connected Sphere

```julia
using Makie

 large_sphere = Sphere(Point3f0(0), 1f0)
 positions = decompose(Point3f0, large_sphere)
 linepos = view(positions, rand(1:length(positions), 1000))
 scene = lines(linepos, linewidth = 0.1, color = :black)
 scatter!(scene, positions, strokewidth = 10, strokecolor = :white, color = RGBAf0(0.9, 0.2, 0.4, 0.6))
 scene


```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="https://raw.githubusercontent.com/SimonDanisch/ReferenceImages/master/gallery/connected_sphere/media/image.jpg" alt="">

    </p>
</div>

```
