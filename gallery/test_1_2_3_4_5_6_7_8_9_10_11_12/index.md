## Test

```julia
using Makie
 using Makie, GeometryTypes

 s1 = GLNormalUVMesh(Sphere(Point3f0(0), 1f0))
 Makie.mesh(GLNormalUVMesh(Sphere(Point3f0(0), 1f0)), color = rand(50, 50))
 # ugh, bug In GeometryTypes for UVs of non unit spheres.
 s2 = GLNormalUVMesh(Sphere(Point3f0(0), 1f0))
 s2.vertices .= s2.vertices .+ (Point3f0(0, 2, 0),)
 mesh!(s2, color = rand(RGBAf0, 50, 50))


```
```@raw html

<div style="display:inline-block"><p style="display:inline-block; text-align: center">1<br><img src="/home/sd/ReferenceImages/recordings/test_1_2_3_4_5_6_7_8_9_10_11_12/media/image.jpg" alt="1<br>">
</p></div>
```