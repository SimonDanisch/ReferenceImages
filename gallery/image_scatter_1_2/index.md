## image scatter

```julia
using Makie
 using LinearAlgebra

 scatter(
     1:10, 1:10, rand(10, 10) .* 10,
     rotations = normalize.(rand(Quaternionf0, 10*10)),
     markersize = 1,
     # can also be an array of images for each point
     # need to be the same size for best performance, though
     marker = Makie.logo()
 )


```
```@raw html

<div style="display:inline-block"><p style="display:inline-block; text-align: center">1<br><img src="/home/sd/ReferenceImages/recordings/image_scatter_1_2/media/image.jpg" alt="1<br>">
</p></div>
```
