## Add and change points

```julia
using Makie
 using LinearAlgebra

 img = rand(100, 100)
 scene = Scene(scale_plot = false, resolution = (500, 500))
 heatmap!(scene, img)
 clicks = Node(Point2f0[(0, 0)])
 blues = Node(Point2f0[])
 on(scene.events.mousebuttons) do buttons
     if ispressed(scene, Mouse.left)
         pos = to_world(scene, Point2f0(scene.events.mouseposition[]))
         found = -1
         c = clicks[]
         for i in 1:length(c)
            if norm(pos - c[i]) < 1
                found = i
            end
         end
         if found >= 1
             blues[] = push!(blues[], pos)
             deleteat!(clicks[], found)
         else
             push!(clicks[], pos)
         end
         clicks[] = clicks[]
    end
    return
 end
 t = Theme(markersize = 10, raw = true)
 scatter!(scene, t, clicks, color = :red, marker = '+')
 red_clicks = scene[end]
 scatter!(scene, t, blues, color = :blue, marker = 'o')
 center!(scene)
 RecordEvents(scene, "output")


```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <video controls autoplay loop muted>
  <source src="/home/sd/.julia/dev/MakieGallery/test/test_recordings/add_and_change_points/media/video.mp4" type="video/mp4">
  Your browser does not support mp4. Please use a modern browser like Chrome or Firefox.
</video>

    </p>
</div>

```
