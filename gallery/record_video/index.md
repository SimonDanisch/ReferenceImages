## Record Video

```julia
using Makie

 scene = Scene()

 f(t, v, s) = (sin(v + t) * s, cos(v + t) * s, (cos(v + t) + sin(v)) * s)
 t = Node(Base.time()) # create a life signal
 limits = FRect3D(Vec3f0(-1.5, -1.5, -3), Vec3f0(3, 3, 6))
 p1 = meshscatter!(scene, lift(t-> f.(t, range(0, stop = 2pi, length = 50), 1), t), markersize = 0.05)[end]
 p2 = meshscatter!(scene, lift(t-> f.(t * 2.0, range(0, stop = 2pi, length = 50), 1.5), t), markersize = 0.05)[end]

 lines = lift(p1[1], p2[1]) do pos1, pos2
     map((a, b)-> (a, b), pos1, pos2)
 end
 linesegments!(scene, lines, linestyle = :dot, limits = limits)
 # record a video
 N = 150
 record(scene, "output.mp4", 1:N) do i
     push!(t, Base.time())
end


```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <video controls autoplay loop muted>
  <source src="https://raw.githubusercontent.com/SimonDanisch/ReferenceImages/master/gallery/record_video/media/record_video.mp4" type="video/mp4">
  Your browser does not support mp4. Please use a modern browser like Chrome or Firefox.
</video>

    </p>
</div>

```
