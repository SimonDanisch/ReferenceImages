## Textured Mesh

```julia
using Makie
 using FileIO

 scene = Scene(resolution = (500, 500))
 catmesh = FileIO.load(Makie.assetpath("cat.obj"), GLNormalUVMesh)
 mesh(catmesh, color = Makie.loadasset("diffusemap.tga"))


```
```@raw html

<div style="display:inline-block"><p style="display:inline-block; text-align: center">1<br><img src="/home/sd/ReferenceImages/recordings/textured_mesh/media/image.jpg" alt="1<br>">
</p></div>
```
