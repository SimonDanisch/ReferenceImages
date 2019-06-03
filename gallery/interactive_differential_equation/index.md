## Interactive Differential Equation

```julia
using AbstractPlotting
 using DifferentialEquations, ParameterizedFunctions
 import AbstractPlotting: textslider

 lorenz = @ode_def Lorenz begin           # define the system
     dx = σ * (y - x)
     dy = x * (ρ - z) - y
     dz = x * y - β*z
 end σ ρ β

 u0 = [1.0,0.0,0.0]                       # initial conditions
 tspan0 = (0.0,100.0)                      # initial timespan
 p0 = [10.0,28.0,8/3]                      # initial parameters
 prob = ODEProblem(lorenz, u0, tspan0, p0)  # define the problem

 ## setup sliders and plotting

 "The order of magnitude to range between."
 OME = 8

 sσ, oσ = textslider(exp10.(-OME:0.001:OME), "σ", start = p0[1]);

 sρ, oρ = textslider(exp10.(-OME:0.001:OME), "ρ", start = p0[2]);

 sβ, oβ = textslider(exp10.(-OME:0.001:OME), "β", start = p0[3]);

 st, ot = textslider(exp10.(-OME:0.001:OME), "tₘₐₓ", start = tspan0[end]);

 sr, or = textslider(100:10000, "resolution", start = 2000);

 trange = lift(ot, or) do tmax, resolution
     LinRange(0.0, tmax, resolution)
 end

 data = lift(oσ, oρ, oβ, trange) do σ, ρ, β, ts
     Point3f0.(
         solve(
             remake(
                 prob;
                 p = [σ, ρ, β],
                 tspan = (ts[1], ts[end])
             )
         )(ts).u
     )  # change to fit the dimensionality - maybe even return 2 arrays, or a set of `Point2`s...
 end
 parent = Scene(resolution = (1000, 500))
 three = lines(data, linewidth = 1, transparency = true, color = ("#fe4a49", 0.6))
 meshscatter!(three, data, markersize = 0.1, color = :gray)
 scene = vbox(hbox(sσ, sρ, sβ, st, sr), three, parent = parent)
 RecordEvents(scene, "output")


```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <video controls autoplay loop muted>
  <source src="https://simondanisch.github.io/ReferenceImages/gallery//interactive_differential_equation/media/video.mp4" type="video/mp4">
  Your browser does not support mp4. Please use a modern browser like Chrome or Firefox.
</video>

    </p>
</div>

```
