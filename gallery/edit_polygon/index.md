## Edit Polygon

```julia
using Makie

 points = node(:poly, Point2f0[(0, 0), (0.5, 0.5), (1.0, 0.0)])
 scene = Scene(resolution = (500, 500))
 poly!(scene, points, strokewidth = 2, strokecolor = :black, color = :skyblue2, show_axis = false, scale_plot = false)
 scatter!(points, color = :white, strokewidth = 10, markersize = 0.05, strokecolor = :black, raw = true)
 pplot = scene[end]
 push!(points[], Point2f0(0.6, -0.3))
 points[] = points[]
 function add_move!(scene, points, pplot)
     idx = Ref(0); dragstart = Ref(false); startpos = Base.RefValue(Point2f0(0))
     on(events(scene).mousedrag) do drag
         if ispressed(scene, Mouse.left)
             if drag == Mouse.down
                 plot, _idx = Makie.mouse_selection(scene)
                 if plot == pplot
                     idx[] = _idx; dragstart[] = true
                     startpos[] = to_world(scene, Point2f0(scene.events.mouseposition[]))
                 end
             elseif drag == Mouse.pressed && dragstart[] && checkbounds(Bool, points[], idx[])
                 pos = to_world(scene, Point2f0(scene.events.mouseposition[]))
                 points[][idx[]] = pos
                 points[] = points[]
             end
         else
             dragstart[] = false
         end
         return
     end
 end

 function add_remove_add!(scene, points, pplot)
     on(events(scene).mousebuttons) do but
         if ispressed(but, Mouse.left) && ispressed(scene, Keyboard.left_control)
             pos = to_world(scene, Point2f0(events(scene).mouseposition[]))
             push!(points[], pos)
             points[] = points[]
         elseif ispressed(but, Mouse.right)
             plot, idx = Makie.mouse_selection(scene)
             if plot == pplot && checkbounds(Bool, points[], idx)
                 deleteat!(points[], idx)
                 points[] = points[]
             end
         end
         return
     end
 end
 add_move!(scene, points, pplot)
 add_remove_add!(scene, points, pplot)
 center!(scene)
 RecordEvents(scene, "output")


```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <video controls autoplay loop muted>
  <source src="https://raw.githubusercontent.com/SimonDanisch/ReferenceImages/master/gallery/edit_polygon/media/video.mp4" type="video/mp4">
  Your browser does not support mp4. Please use a modern browser like Chrome or Firefox.
</video>

    </p>
</div>

```
