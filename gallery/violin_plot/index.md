## Violin plot

```julia
using AbstractPlotting
 using RDatasets, StatsMakie


 d = dataset("Ecdat", "Fatality");

 violin(Data(d), :Year, :Perinc)



```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="https://simondanisch.github.io/ReferenceImages/gallery//violin_plot/media/image.jpg" alt="">

    </p>
</div>

```
