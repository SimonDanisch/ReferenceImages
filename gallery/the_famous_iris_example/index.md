## The famous iris example

```julia
using Makie
 using DataFrames, RDatasets # do Pkg.add.(["DataFrames", "RDatasets"]) if you don't have these packages installed

 iris = dataset("datasets", "iris")

 x = iris[:SepalWidth]
 y = iris[:SepalLength]

 scene = Scene()
 colors = [:red, :green, :blue]
 i = 1 #color incrementer
 for sp in unique(iris[:Species])
     idx = iris[:Species] .== sp
     sel = iris[idx, [:SepalWidth, :SepalLength]]
     scatter!(scene, sel[:,1], sel[:,2], color = colors[i], limits = FRect(1.5, 4.0, 3.0, 4.0))
     global i = i+1
 end
 scene
 axis = scene[Axis] # get axis
 axis[:names][:axisnames] = ("Sepal width", "Sepal length")
 scene


```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="https://raw.githubusercontent.com/SimonDanisch/ReferenceImages/master/gallery/the_famous_iris_example/media/image.jpg" alt="">

    </p>
</div>

```
