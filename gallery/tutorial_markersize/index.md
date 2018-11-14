## Tutorial markersize

```julia
using Makie

 x = 1:10
 y = 1:10
 sizevec = [s for s = 1:length(x)] ./ 10

 scene = scatter(x, y, markersize = sizevec)


```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="https://raw.githubusercontent.com/SimonDanisch/ReferenceImages/master/gallery/tutorial_markersize/media/image.jpg" alt="">

    </p>
</div>

```
