## pulsing marker

```julia
using Makie

 N = 100
 scene = scatter([0], [0], marker = '❤', markersize = 0.5, color = :red, raw = true)
 s = scene[end] # last plot in scene
 record(scene, "output.mp4", range(0, stop = 10pi, length = N)) do i
     s[:markersize] = (cos(i) + 1) / 4 + 0.2
end


```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <video controls autoplay loop muted>
  <source src="/home/sd/.julia/dev/MakieGallery/test/test_recordings/pulsing_marker/media/pulsing_marker.mp4" type="video/mp4">
  Your browser does not support mp4. Please use a modern browser like Chrome or Firefox.
</video>

    </p>
</div>

```
