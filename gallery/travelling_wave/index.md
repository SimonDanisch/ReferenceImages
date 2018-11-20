## Travelling wave

```julia
using Makie

 scene = Scene()
 mytime = Node(0.0)
 f(v, t) = sin(v + t)
 scene = lines!(
     scene,
     lift(t -> f.(range(0, stop = 2pi, length = 50), t), mytime),
     color = :blue)
 p1 = scene[end];
 N = 100
 record(scene, "output.mp4", range(0, stop = 4pi, length = N)) do i
     mytime[] = i
end


```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <video controls autoplay loop muted>
  <source src="/home/sd/.julia/dev/MakieGallery/test/test_recordings/travelling_wave/media/travelling_wave.mp4" type="video/mp4">
  Your browser does not support mp4. Please use a modern browser like Chrome or Firefox.
</video>

    </p>
</div>

```
