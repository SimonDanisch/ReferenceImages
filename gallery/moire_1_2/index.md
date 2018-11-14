## Moire

```julia
using Makie

 function cartesian(ll)
     return Point3f0(
         cos(ll[1]) * sin(ll[2]),
         sin(ll[1]) * sin(ll[2]),
         cos(ll[2])
     )
 end
 fract(x) = x - floor(x)
 function calcpositions(rings, index, time, audio)
     movement, radius, speed, spin = 1, 2, 3, 4;
     position = Point3f0(0.0)
     precision = 0.2f0
     for ring in rings
         position += ring[radius] * cartesian(
             precision *
             index *
             Point2f0(ring[spin] + Point2f0(sin(time * ring[speed]), cos(time * ring[speed])) * ring[movement])
         )
     end
     amplitude = audio[round(Int, clamp(fract(position[1] * 0.1), 0, 1) * (25000-1)) + 1]; # index * 0.002
     position *= 1.0 + amplitude * 0.5;
     position
 end
 rings = [(0.1f0, 1.0f0, 0.00001f0, Point2f0(0.2, 0.1)), (0.1f0, 0.0f0, 0.0002f0, Point2f0(0.052, 0.05))]
 N2 = 25000
 t_audio = sin.(range(0, stop = 10pi, length = N2)) .+ (cos.(range(-3, stop = 7pi, length = N2)) .* 0.6) .+ (rand(Float32, N2) .* 0.1) ./ 2f0
 start = time()
 t = (time() - start) * 100
 pos = calcpositions.((rings,), 1:N2, t, (t_audio,))

 scene = lines(pos, color = RGBAf0.(to_colormap(:RdBu, N2), 0.6), thickness = 0.6f0, show_axis = false)
 linesegments!(scene, FRect3D(Vec3f0(-1.5), Vec3f0(3)), raw = true, linewidth = 3, linestyle = :dot)
 eyepos = Vec3f0(5, 1.5, 0.5)
 lookat = Vec3f0(0)
 update_cam!(scene, eyepos, lookat)
 l = scene[1]
 N = 150
 record(scene, "output.mp4", 1:N) do i
     t = (time() - start) * 700
     pos .= calcpositions.((rings,), 1:N2, t, (t_audio,))
     l[1] = pos # update argument 1
     rotate_cam!(scene, 0.0, 0.01, 0.01)
end


```
```@raw html

<div style="display:inline-block"><p style="display:inline-block; text-align: center">1<br><video controls autoplay loop muted>
  <source src="/home/sd/ReferenceImages/recordings/moire_1_2/media/moire_1_2.mp4" type="video/mp4">
  Your browser does not support mp4. Please use a modern browser like Chrome or Firefox.
</video>
</p></div>
```
