## Labels

```julia
using Makie
 using Makie

 scene = Scene(resolution = (500, 500))
 x = map([:dot, :dash, :dashdot], [2, 3, 4]) do ls, lw
     linesegments!(
         range(1, stop = 5, length = 100), rand(100), rand(100),
         linestyle = ls, linewidth = lw,
         color = rand(RGBAf0)
     )[end]
 end
 x = [x..., scatter!(range(1, stop=5, length=100), rand(100), rand(100))[end]]
 center!(scene)
 ls = Makie.legend(x, ["attribute $i" for i in 1:4], camera = campixel!, raw = true)

 st = Stepper(vbox(scene, ls), "output")
 l = ls[end]
 l[:strokecolor] = RGBAf0(0.8, 0.8, 0.8)
 step!(st)
 l[:gap] = 15
 step!(st)
 l[:textsize] = 12
 step!(st)
 l[:linepattern] = Point2f0[(0,-0.2), (0.5, 0.2), (0.5, 0.2), (1.0, -0.2)]
 step!(st)
 l[:scatterpattern] = decompose(Point2f0, Circle(Point2f0(0.5, 0), 0.3f0), 9)
 l[:markersize] = 2f0
 step!(st)
 st


```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="https://raw.githubusercontent.com/SimonDanisch/ReferenceImages/master/gallery/labels/media/labels-1.jpg" alt="">

    </p>
</div>

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="https://raw.githubusercontent.com/SimonDanisch/ReferenceImages/master/gallery/labels/media/labels-2.jpg" alt="">

    </p>
</div>

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="https://raw.githubusercontent.com/SimonDanisch/ReferenceImages/master/gallery/labels/media/labels-3.jpg" alt="">

    </p>
</div>

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="https://raw.githubusercontent.com/SimonDanisch/ReferenceImages/master/gallery/labels/media/labels-4.jpg" alt="">

    </p>
</div>

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="https://raw.githubusercontent.com/SimonDanisch/ReferenceImages/master/gallery/labels/media/labels-5.jpg" alt="">

    </p>
</div>

```
