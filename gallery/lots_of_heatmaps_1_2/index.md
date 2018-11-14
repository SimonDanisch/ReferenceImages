## Lots of Heatmaps

```julia
using Makie

 function makeheatmaps(bufs)
     heatmaps = map(bufs) do buf
         heatmap(
             buf, padding = (0,0), colorrange = (0,1),
             axis = (names = (axisnames = ("", ""),),)
         )
     end
     scene = hbox(map(i-> vbox(heatmaps[i, :]), 1:size(bufs, 1))...)
     scene, last.(heatmaps)
 end
 datarows = 500; datacols = 500
 plotrows = 4; plotcols = 4
 bufs = [fill(0.0f0, datarows, datacols) for _ in 1:plotrows, _ in 1:plotcols]
 scene, hms = makeheatmaps(bufs)
 N = 100
 record(scene, "output.mp4", 1:N) do i
     for (hm, buf) in zip(vec(hms), vec(bufs))
         buf .= rand.(Float32)
         hm[1] = buf
     end
     yield()
end


```
```@raw html

<div style="display:inline-block"><p style="display:inline-block; text-align: center">1<br><video controls autoplay loop muted>
  <source src="/home/sd/ReferenceImages/recordings/lots_of_heatmaps_1_2/media/lots_of_heatmaps_1_2.mp4" type="video/mp4">
  Your browser does not support mp4. Please use a modern browser like Chrome or Firefox.
</video>
</p></div>
```
