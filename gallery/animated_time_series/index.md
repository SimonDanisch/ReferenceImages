## Animated time series

```julia
using AbstractPlotting

 f0 = 1/2; fs = 100;
 winsec = 4; hopsec = 1/60
 nwin = round(Integer, winsec*fs)
 nhop = round(Integer, hopsec*fs)
 # do the loop
 frame_start = -winsec
 frame_time = collect((0:(nwin-1)) * (1/fs))
 aframe = sin.(2*pi*f0.*(frame_start .+ frame_time))
 scene = lines(frame_start .+ frame_time, aframe)
 center!(scene)
 lineplot = scene[end]
 fix = 0
 record(scene, "output.mp4", 1:50) do i
     global frame_start
     aframe .= sin.(2*pi*f0.*(frame_start .+ frame_time))
     # append!(aframe, randn(nhop)); deleteat!(aframe, 1:nhop)
     lineplot[1] = frame_start .+ frame_time
     lineplot[2] = aframe
     AbstractPlotting.update_limits!(scene)
     AbstractPlotting.update!(scene)
     sleep(hopsec)
     frame_start += hopsec
end


```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <video controls autoplay loop muted>
  <source src="https://simondanisch.github.io/ReferenceImages/gallery//animated_time_series/media/animated_time_series.mp4" type="video/mp4">
  Your browser does not support mp4. Please use a modern browser like Chrome or Firefox.
</video>

    </p>
</div>

```
