## Line Function

```julia
using Makie

 scene = Scene()
 x = range(0, stop = 3pi)
 lines!(scene, x, sin.(x))
 lines!(scene, x, cos.(x), color = :blue)


```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="/home/sd/.julia/dev/MakieGallery/test/test_recordings/line_function/media/image.jpg" alt="">

    </p>
</div>

```
