## Test

```julia
using AbstractPlotting
 using GeometryTypes

 s1 = GLNormalUVMesh(Sphere(Point3f0(0), 1f0))
 mesh(GLNormalUVMesh(Sphere(Point3f0(0), 1f0)), color = rand(50, 50))
 # ugh, bug In GeometryTypes for UVs of non unit spheres.
 s2 = GLNormalUVMesh(Sphere(Point3f0(0), 1f0))
 s2.vertices .= s2.vertices .+ (Point3f0(0, 2, 0),)
 mesh!(s2, color = rand(RGBAf0, 50, 50))


```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="https://simondanisch.github.io/ReferenceImages/gallery//test_15/media/image.jpg" alt="">

    </p>
</div>

```
