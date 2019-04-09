## Line GIF

```julia
using AbstractPlotting
 using GLMakie

 us = range(0, stop = 1, length = 100)
 scene = Scene()
 scene = linesegments!(scene, FRect3D(Vec3f0(0, -1, 0), Vec3f0(1, 2, 2)))
 p = lines!(scene, us, sin.(us .+ time()), zeros(100), linewidth = 3, transparency = true)[end]
 lineplots = [p]
 translate!(p, 0, 0, 0)
 colors = to_colormap(:RdYlBu)
 #display(scene) # would be needed without the record
 N = 150
 path = record(scene, "test.gif", 1:N) do i
     global lineplots, scene
     if length(lineplots) < 20
         p = lines!(
             scene,
             us, sin.(us .+ time()), zeros(100),
             color = colors[length(lineplots)],
             linewidth = 3
         )[end]
         pushfirst!(lineplots, p)
         translate!(p, 0, 0, 0)
         #TODO automatically insert new plots
         insert!(GLMakie.global_gl_screen(), scene, p)
     else
         lineplots = circshift(lineplots, 1)
         lp = first(lineplots)
         lp[2] = sin.(us .+ time())
         translate!(lp, 0, 0, 0)
     end
     for lp in Iterators.drop(lineplots, 1)
         z = translation(lp)[][3]
         translate!(lp, 0, 0, z + 0.1)
     end
 end
 path


```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="https://simondanisch.github.io/ReferenceImages/gallery//line_gif/media/test.gif" alt="">

    </p>
</div>

```
