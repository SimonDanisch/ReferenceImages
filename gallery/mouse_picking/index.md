## Mouse Picking

```julia
using Makie

 img = rand(100, 100)
 scene = Scene(resolution = (500, 500))
 heatmap!(scene, img, scale_plot = false)
 clicks = Node(Point2f0[(0,0)])
 on(scene.events.mousebuttons) do buttons
    if ispressed(scene, Mouse.left)
        pos = to_world(scene, Point2f0(scene.events.mouseposition[]))
        push!(clicks, push!(clicks[], pos))
    end
    return
 end
 scatter!(scene, clicks, color = :red, marker = '+', markersize = 10)
 RecordEvents(scene, "output")


```
```@raw html

<div style="display:inline-block"><p style="display:inline-block; text-align: center">1<br><video controls autoplay loop muted>
  <source src="/home/sd/ReferenceImages/recordings/mouse_picking/media/video.mp4" type="video/mp4">
  Your browser does not support mp4. Please use a modern browser like Chrome or Firefox.
</video>
</p></div>
```
