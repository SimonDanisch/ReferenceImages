## Interaction with Mouse

```julia
using AbstractPlotting
 using LinearAlgebra

 scene = Scene(raw = true, camera = cam2d!, resolution = (500, 500))
 r = range(0, stop = 3, length = 4)
 the_time = Node(time())
 last_open = false
 @async while true
     global last_open
     the_time[] = time()
     # this is a bit awkward, since the isopen(scene) is false
     # as long as the scene isn't displayed
     last_open && !isopen(scene) && break
     last_open = isopen(scene)
     sleep(1/25)
 end
 pos = lift(scene.events.mouseposition, the_time) do mpos, t
     map(LinRange(0, 2pi, 60)) do i
         circle = Point2f0(sin(i), cos(i))
         mouse = to_world(scene, Point2f0(mpos))
         secondary = (sin((i * 10f0) + t) * 0.09) * normalize(circle)
         (secondary .+ circle) .+ mouse
     end
 end
 lines!(scene, pos)
 p1 = scene[end]
 p2 = scatter!(
     scene,
     pos, markersize = 0.1f0,
     marker = :star5,
     color = p1[:color],
 )[end]
 center!(scene)
 t = Theme(raw = true, camera = campixel!)
 b1 = button(t, "color")
 b2 = button(t, "marker")
 msize = slider(t, 0.1:0.01:0.5)
 on(b1[end][:clicks]) do c
     p1[:color] = rand(RGBAf0)
 end
 markers = ('π', '😹', '⚃', '◑', '▼')
 on(b2[end][:clicks]) do c
     p2[:marker] = markers[rand(1:5)]
 end
 on(msize[end][:value]) do val
     p2[:markersize] = val
 end
 RecordEvents(hbox(
     vbox(b1, b2, msize),
     scene
 ), "output")


```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <video controls autoplay loop muted>
  <source src="https://simondanisch.github.io/ReferenceImages/gallery/\\interaction_with_mouse\\media\\video.mp4" type="video/mp4">
  Your browser does not support mp4. Please use a modern browser like Chrome or Firefox.
</video>

    </p>
</div>

```
