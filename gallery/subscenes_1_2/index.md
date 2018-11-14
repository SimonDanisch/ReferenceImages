## Subscenes

```julia
using Makie

 img = rand(RGBAf0, 100, 100)
 scene = image(img, show_axis = false)
 subscene = Scene(scene, IRect(100, 100, 300, 300))
 scatter!(subscene, rand(100) * 200, rand(100) * 200, markersize = 4)
 scene


```
```@raw html

<div style="display:inline-block"><p style="display:inline-block; text-align: center">1<br><img src="/home/sd/ReferenceImages/recordings/subscenes_1_2/media/image.jpg" alt="1<br>">
</p></div>
```
