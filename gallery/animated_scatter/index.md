## Animated Scatter

```julia
using AbstractPlotting

 N = 10
 r = [(rand(7, 2) .- 0.5) .* 25 for i = 1:N]
 scene = scatter(r[1][:, 1], r[1][:, 2], markersize = 1, limits = FRect(-25/2, -25/2, 25, 25))
 s = scene[end] # last plot in scene
 record(scene, "output.mp4", r) do m
     s[1] = m[:, 1]
     s[2] = m[:, 2]
end


```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <video controls autoplay loop muted>
  <source src="https://simondanisch.github.io/ReferenceImages/gallery/\\animated_scatter\\media\\animated_scatter.mp4" type="video/mp4">
  Your browser does not support mp4. Please use a modern browser like Chrome or Firefox.
</video>

    </p>
</div>

```
