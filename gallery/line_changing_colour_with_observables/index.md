## Line changing colour with Observables

```julia
using AbstractPlotting

 "'Time' - an Observable that controls the animation"
 t = Node(0)

 "The colour of the line"
 c = lift(t) do t
         RGBf0(t/255, (255 - t)/255, 0)
     end

 scene = lines(rand(10); linewidth=10, color = c)

 record(scene, "output.mp4", 1:255; framerate = 60) do i
     t[] = i # update `t`'s value
end


```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <video controls autoplay loop muted>
  <source src="https://simondanisch.github.io/ReferenceImages/gallery//line_changing_colour_with_observables/media/line_changing_colour_with_observables.mp4" type="video/mp4">
  Your browser does not support mp4. Please use a modern browser like Chrome or Firefox.
</video>

    </p>
</div>

```
