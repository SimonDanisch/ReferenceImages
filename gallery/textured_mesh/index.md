## Textured Mesh

```julia
using Makie
 using FileIO

 scene = Scene(resolution = (500, 500))
 catmesh = FileIO.load(Makie.assetpath("cat.obj"), GLNormalUVMesh)
 mesh(catmesh, color = Makie.loadasset("diffusemap.tga"))


```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="https://raw.githubusercontent.com/SimonDanisch/ReferenceImages/master/gallery/textured_mesh/media/image.jpg" alt="">

    </p>
</div>

```
