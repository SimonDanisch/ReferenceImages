## Test

```julia
using Makie

 scene = Scene(raw = true, camera = campixel!)
 text!(
     scene, "boundingbox",
     align = (:left, :center),
     position = (200, 50)
 )
 scale!(scene, Vec3f0(4, 1, 1))
 linesegments!(boundingbox(scene))
 offset = 0
 for a_lign in (:center, :left, :right), b_lign in (:center, :left, :right)
     global offset
     t = text!(
         "boundingbox",
         align = (a_lign, b_lign),
         position = (200, 100 + offset)
     )[end]
     linesegments!(boundingbox(t))
     offset += 50
 end
 scene


```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="https://raw.githubusercontent.com/SimonDanisch/ReferenceImages/master/gallery/test/media/image.jpg" alt="">

    </p>
</div>

```
