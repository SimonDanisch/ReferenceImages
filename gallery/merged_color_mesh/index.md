## Merged color Mesh

```julia
using AbstractPlotting
 using GeometryTypes

 x = Vec3f0(0); baselen = 0.2f0; dirlen = 1f0
 # create an array of differently colored boxes in the direction of the 3 axes
 rectangles = [
     (HyperRectangle(Vec3f0(x), Vec3f0(dirlen, baselen, baselen)), RGBAf0(1,0,0,1)),
     (HyperRectangle(Vec3f0(x), Vec3f0(baselen, dirlen, baselen)), RGBAf0(0,1,0,1)),
     (HyperRectangle(Vec3f0(x), Vec3f0(baselen, baselen, dirlen)), RGBAf0(0,0,1,1))
 ]
 meshes = map(GLNormalMesh, rectangles)
 mesh(merge(meshes))


```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="https://simondanisch.github.io/ReferenceImages/gallerymerged_color_mesh/media/image.jpg" alt="">

    </p>
</div>

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="https://simondanisch.github.io/ReferenceImages/gallerymerged_color_mesh/media/thumb.jpg" alt="">

    </p>
</div>

```
