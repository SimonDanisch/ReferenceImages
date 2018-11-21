## Animated surface and wireframe

```julia
using Makie

 scene = Scene();
 function xy_data(x, y)
     r = sqrt(x^2 + y^2)
     r == 0.0 ? 1f0 : (sin(r)/r)
 end

 r = range(-2, stop = 2, length = 50)
 surf_func(i) = [Float32(xy_data(x*i, y*i)) for x = r, y = r]
 z = surf_func(20)
 surf = surface!(scene, r, r, z)[end]

 wf = wireframe!(scene, r, r, Makie.lift(x-> x .+ 1.0, surf[3]),
     linewidth = 2f0, color = Makie.lift(x-> to_colormap(x)[5], surf[:colormap])
 )
 N = 150
 scene
 record(scene, "output.mp4", range(5, stop = 40, length = N)) do i
     surf[3] = surf_func(i)
end


```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <video controls autoplay loop muted>
  <source src="https://raw.githubusercontent.com/SimonDanisch/ReferenceImages/master/gallery/animated_surface_and_wireframe/media/animated_surface_and_wireframe.mp4" type="video/mp4">
  Your browser does not support mp4. Please use a modern browser like Chrome or Firefox.
</video>

    </p>
</div>

```
