## Image on Surface Sphere

```julia
using Makie

 n = 20
 θ = [0;(0.5:n-0.5)/n;1]
 φ = [(0:2n-2)*2/(2n-1);2]
 x = [cospi(φ)*sinpi(θ) for θ in θ, φ in φ]
 y = [sinpi(φ)*sinpi(θ) for θ in θ, φ in φ]
 z = [cospi(θ) for θ in θ, φ in φ]
 rand([-1f0, 1f0], 3)
 pts = vec(Point3f0.(x, y, z))
 surface(x, y, z, color = Makie.logo())


```
```@raw html

<div style="display:inline-block"><p style="display:inline-block; text-align: center">1<br><img src="/home/sd/ReferenceImages/recordings/image_on_surface_sphere_1_2/media/image.jpg" alt="1<br>">
</p></div>
```
