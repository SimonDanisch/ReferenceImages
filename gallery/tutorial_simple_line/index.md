## Tutorial simple line

```julia
using Makie

 x = range(0, stop = 2pi, length = 40)
 f(x) = sin.(x)
 y = f(x)
 scene = lines(x, y, color = :blue)


```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="/home/sd/.julia/dev/MakieGallery/test/test_recordings/tutorial_simple_line/media/image.jpg" alt="">

    </p>
</div>

```
