## Volume on black background

```julia
using AbstractPlotting

 r = LinRange(-3, 3, 100);  # our value range

 ρ(x, y, z) = exp(-(abs(x))) # function (charge density)

 # create a Scene with the attribute `backgroundcolor = :black`,
 # can be any compatible color.  Useful for better contrast and not killing your eyes with a white background.
 scene = Scene(backgroundcolor = :black)

 volume!(
     scene,
     r, r, r,          # coordinates to plot on
     ρ,                # charge density (functions as colorant)
     algorithm = :mip  # maximum-intensity-projection
 )

 scene[Axis].names.textcolor = :gray # let axis labels be seen on dark background

 scene # show scene


```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="https://simondanisch.github.io/ReferenceImages/gallery//volume_on_black_background/media/image.jpg" alt="">

    </p>
</div>

```
