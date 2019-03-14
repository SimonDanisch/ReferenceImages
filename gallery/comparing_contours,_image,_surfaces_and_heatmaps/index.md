## Comparing contours, image, surfaces and heatmaps

```julia
using AbstractPlotting, GLMakie, GLMakie

 N = 20
 x = LinRange(-0.3, 1, N)
 y = LinRange(-1, 0.5, N)
 z = x .* y'
 hbox(
     vbox(
         contour(x, y, z, levels = 20, linewidth =3),
         contour(x, y, z, levels = 0, linewidth = 0, fillrange = true),
         heatmap(x, y, z),
     ),
     vbox(
         image(x, y, z, colormap = :viridis),
         surface(x, y, fill(0f0, N, N), color = z, shading = false),
         image(-0.3..1, -1..0.5, AbstractPlotting.logo())
     )
 )


```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="https://simondanisch.github.io/ReferenceImages/gallery//comparing_contours,_image,_surfaces_and_heatmaps/media/image.jpg" alt="">

    </p>
</div>

```
