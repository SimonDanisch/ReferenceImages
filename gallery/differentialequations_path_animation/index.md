## DifferentialEquations path animation

```julia
using AbstractPlotting
 using OrdinaryDiffEq
 using Statistics


 function lorenz(du,u,p,t)
     du[1] = 10.0*(u[2]-u[1])
     du[2] = u[1]*(28.0-u[3]) - u[2]
     du[3] = u[1]*u[2] - (8/3)*u[3]
 end

 u0 = [1.0; 0.0; 0.0]
 tspan = (0.0, 10.0)
 prob = ODEProblem(lorenz, u0, tspan)
 sol = solve(prob, Tsit5())

 t = Node(tspan[1])
 trajectory = lift(t; init = [Point3f0(sol(t[], idxs = [1,2,3]))]) do t
     push!(trajectory[], Point3f0(sol(t, idxs=[1,2,3])))
 end
 endpoint = lift(t->[Point3f0(sol(t, idxs = [1,2,3]))], t)

 xm, xM = extrema(sol[1,:])
 ym, yM = extrema(sol[2,:])
 zm, zM = extrema(sol[3,:])

 limits = FRect3D((xm,ym,zm), (xM-xm,yM-ym,zM-zm))

 scene = lines(trajectory, limits = limits, markersize = 0.7)
 meshscatter!(scene, endpoint, limits = limits, markersize = 0.5, color = :red)
 eyepos = Vec3f0(100, 5.0, 25)
 N = 1000
 record(scene, "output.mp4", LinRange(tspan..., N)) do tᵢ
     global eyepos
     push!(t, tᵢ)
     eyepos = Vec3f0(eyepos[1] - (N / 10000), eyepos[2], eyepos[3])
     update_cam!(scene, eyepos, mean(trajectory[]))
     sleep(0.001)
end


```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <video controls autoplay loop muted>
  <source src="https://simondanisch.github.io/ReferenceImages/gallery//differentialequations_path_animation/media/differentialequations_path_animation.mp4" type="video/mp4">
  Your browser does not support mp4. Please use a modern browser like Chrome or Firefox.
</video>

    </p>
</div>

```
