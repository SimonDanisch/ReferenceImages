## Text rotation

```julia
using Makie

 scene = Scene()
 pos = (500, 500)
 posis = Point2f0[]
 for r in range(0, stop = 2pi, length = 20)
     global pos, posis
     p = pos .+ (sin(r)*100.0, cos(r) * 100)
     push!(posis, p)
     t = text!(
         scene, "test",
         position = p,
         textsize = 50,
         rotation = 1.5pi - r,
         align = (:center, :center)
     )
 end
 scatter!(scene, posis, markersize = 10)


```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="/home/sd/.julia/dev/MakieGallery/test/test_recordings/text_rotation/media/image.jpg" alt="">

    </p>
</div>

```
