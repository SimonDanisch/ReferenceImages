## Hbox

```julia
using Makie

 t = range(-122277.93103448274, stop=-14798.035304081845, length=29542)
 x = -42 .- randn(length(t))
 sc1 = scatter(t, x, color=:black, markersize=sqrt(length(t)/20))
 sc2 = lines(t[1:end-1], diff(x), color = :blue)
 hbox(sc2, sc1)


```
```@raw html

<div style="display:inline-block"><p style="display:inline-block; text-align: center">1<br><img src="/home/sd/ReferenceImages/recordings/hbox_1_2_3/media/image.jpg" alt="1<br>">
</p></div>
```
