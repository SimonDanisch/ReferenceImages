## Tutorial markersize

```julia
using Makie

 x = 1:10
 y = 1:10
 sizevec = [s for s = 1:length(x)] ./ 10

 scene = scatter(x, y, markersize = sizevec)


```
```@raw html

<div style="display:inline-block"><p style="display:inline-block; text-align: center">1<br><img src="/home/sd/ReferenceImages/recordings/tutorial_markersize/media/image.jpg" alt="1<br>">
</p></div>
```
