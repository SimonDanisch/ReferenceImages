## Violin and box plot

```julia
using AbstractPlotting
 using RDatasets, StatsMakie


 d = dataset("Ecdat","Fatality");

 violin(d.Year, d.Perinc, color = :gray)
 boxplot!(d.Year, d.Perinc, color = :black)



```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="https://simondanisch.github.io/ReferenceImages/gallery//violin_and_box_plot/media/image.jpg" alt="">

    </p>
</div>

```
