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

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="https://raw.githubusercontent.com/SimonDanisch/ReferenceImages/master/gallery/subscenes/media/image.jpg" alt="">

    </p>
</div>

```
