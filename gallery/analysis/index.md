## Analysis

```julia
using AbstractPlotting
 using StatsMakie
 using DataFrames, RDatasets # for data
 using StatsMakie: smooth, linear


 mtcars = dataset("datasets", "mtcars")    # load dataset of car statistics
 iris = dataset("datasets", "iris")

 disallowmissing!.([mtcars, iris])  # convert columns from Union{T, Missing} to T
 # We can use this because the dataset has no missing values.

 @substep

 # kde

 plot(
     density,           # the type of analysis
     Data(mtcars),
     :MPG,
     Group(color = :Cyl)
 )

 @substep

 # histogram

 plot(
     histogram,         # the type of analysis
     Data(mtcars),
     :MPG,
     Group(color = :Cyl)
 )

 @substep

 # frequency analysis

 plot(
     frequency,
     Data(iris),
     :Species
 )

 @substep
 xs = 10 .* rand(100)
 ys = sin.(xs) .+ 0.5 .* rand.()
 scatter(xs, ys)
 plot!(smooth, xs, ys)

 @substep
 scatter(xs, ys)
 plot!(linear, xs, ys)


```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="https://simondanisch.github.io/ReferenceImages/gallery//analysis/media/image2.jpg" alt="">

    </p>
</div>

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="https://simondanisch.github.io/ReferenceImages/gallery//analysis/media/image3.jpg" alt="">

    </p>
</div>

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="https://simondanisch.github.io/ReferenceImages/gallery//analysis/media/image4.jpg" alt="">

    </p>
</div>

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="https://simondanisch.github.io/ReferenceImages/gallery//analysis/media/image5.jpg" alt="">

    </p>
</div>

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="https://simondanisch.github.io/ReferenceImages/gallery//analysis/media/image6.jpg" alt="">

    </p>
</div>

```
