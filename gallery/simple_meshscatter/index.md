## Simple meshscatter

```julia
using Makie

 large_sphere = Sphere(Point3f0(0), 1f0)
 positions = decompose(Point3f0, large_sphere)
 meshscatter(positions, color = RGBAf0(0.9, 0.2, 0.4, 1), markersize = 0.05)


```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="https://raw.githubusercontent.com/SimonDanisch/ReferenceImages/master/gallery/simple_meshscatter/media/image.jpg" alt="">

    </p>
</div>

```
