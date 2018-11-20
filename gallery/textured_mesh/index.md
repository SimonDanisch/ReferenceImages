## Textured Mesh

```julia
using Makie
 using FileIO, GLMakie

 scene = Scene(resolution = (500, 500))
 catmesh = FileIO.load(GLMakie.assetpath("cat.obj"), GLNormalUVMesh)
 mesh(catmesh, color = GLMakie.loadasset("diffusemap.tga"))


```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="/home/sd/.julia/dev/MakieGallery/test/test_recordings/textured_mesh/media/image.jpg" alt="">

    </p>
</div>

```
