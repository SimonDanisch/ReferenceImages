## Errorbar

```julia
using AbstractPlotting
 using StatsMakie

 x = [1:4;]
 y =  [1:4;]
 Δx = fill(0.25, 4)
 Δy = fill(0.25, 4)
 p = errorbar(x,y,Δx,Δy,xcolor=:green, ycolor=:red)


```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="https://simondanisch.github.io/ReferenceImages/gallery//errorbar/media/image.jpg" alt="">

    </p>
</div>

```
