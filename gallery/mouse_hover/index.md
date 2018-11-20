## Mouse Hover

```julia
using Makie
 using Colors, Observables

 r = range(0, stop=5pi, length=100)
 scene = Scene(resolution = (500, 500))
 lines!(scene, r, sin.(r), linewidth = 3)
 lineplot = scene[end]
 visible = node(:visible, false)
 poprect = lift(scene.events.mouseposition) do mp
     FRect((mp .+ 5), 250, 40)
 end
 textpos = lift(scene.events.mouseposition) do mp
     Vec3f0((mp .+ 5 .+ (250/2, 40 / 2))..., 120)
 end
 popup = poly!(campixel(scene), poprect, raw = true, color = :white, strokewidth = 2, strokecolor = :black, visible = visible)
 rect = popup[end]
 translate!(rect, Vec3f0(0, 0, 100))
 text!(popup, "( 0.000,  0.000)", textsize = 30, position = textpos, color = :darkred, align = (:center, :center), raw = true, visible = visible)
 text_field = popup[end]
 scene
 x = Node(false)
 on(scene.events.mouseposition) do event
     plot, idx = Makie.mouse_selection(scene)
     if plot == lineplot && idx > 0
         visible[] = true
         text_field[1] = sprint(io-> print(io, round.(Float64.(Tuple(lineplot[1][][idx])), digits = 3)))
     else
         visible[] = false
     end
     return
 end
 RecordEvents(scene, "output")


```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <video controls autoplay loop muted>
  <source src="/home/sd/.julia/dev/MakieGallery/test/test_recordings/mouse_hover/media/video.mp4" type="video/mp4">
  Your browser does not support mp4. Please use a modern browser like Chrome or Firefox.
</video>

    </p>
</div>

```
