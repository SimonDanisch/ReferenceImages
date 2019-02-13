## Stepper demo

```julia
using AbstractPlotting

 function stepper_demo()
     scene = Scene()
     pos = (50, 50)
     steps = ["Step 1", "Step 2", "Step 3"]
     colors = AbstractPlotting.to_colormap(:Set1, length(steps))
     lines!(scene, Rect(0,0,500,500), linewidth = 0.0001)
     # initialize the stepper and give it an output destination
     st = Stepper(scene, "output")

     for i = 1:length(steps)
         text!(
             scene,
             steps[i],
             position = pos,
             align = (:left, :bottom),
             textsize = 100,
             font = "Blackchancery",
             color = colors[i],
             scale_plot = false
         )
         pos = pos .+ 100
         step!(st) # saves the step and increments the step by one
     end
     st
 end
 stepper_demo()


```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="https://simondanisch.github.io/ReferenceImages/gallery/\\stepper_demo\\media\\stepper_demo-1.jpg" alt="">

    </p>
</div>

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="https://simondanisch.github.io/ReferenceImages/gallery/\\stepper_demo\\media\\stepper_demo-2.jpg" alt="">

    </p>
</div>

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="https://simondanisch.github.io/ReferenceImages/gallery/\\stepper_demo\\media\\stepper_demo-3.jpg" alt="">

    </p>
</div>

```
