## pong

```julia
using AbstractPlotting, GLMakie, GLMakie

 xyvec = rand(Point2f0, (2)) .* 5 .+ 1
 velvec = rand(Point2f0, (2)) .* 10
 # define some other parameters
 t = 0
 ts = 0.03
 balldiameter = 1
 origin = Point2f0(0, 0)
 xybounds = Point2f0(10, 10)
 N = 200
 scene = scatter(
     xyvec,
     markersize = balldiameter,
     color = rand(RGBf0, 2),
     limits = FRect(0, 0, xybounds)
 )
 s = scene[end] # last plot in scene

 record(scene, "output.mp4", 1:N) do i
     # calculate new ball position
     global t = t + ts
     global xyvec = xyvec .+ velvec .* ts
     global velvec = map(xyvec, xybounds, origin, velvec) do p, b, o, vel
         boolvec = ((p .+ balldiameter/2) .> b) .| ((p .- balldiameter/2) .< o)
         velvec = map(boolvec, vel) do b, v
             b ? -v : v
         end
     end
     # plot
     s[1] = xyvec
end


```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <video controls autoplay loop muted>
  <source src="https://simondanisch.github.io/ReferenceImages/gallery//pong/media/pong.mp4" type="video/mp4">
  Your browser does not support mp4. Please use a modern browser like Chrome or Firefox.
</video>

    </p>
</div>

```
