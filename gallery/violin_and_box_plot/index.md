## Violin and box plot

```@raw html
<pre class='hljl'>
<span class='hljl-k'>using</span><span class='hljl-t'> </span><span class='hljl-n'>Makie</span><span class='hljl-t'>
 </span><span class='hljl-k'>using</span><span class='hljl-t'> </span><span class='hljl-n'>RDatasets</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>StatsMakie</span><span class='hljl-t'>


 </span><span class='hljl-n'>d</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>dataset</span><span class='hljl-p'>(</span><span class='hljl-s'>&quot;Ecdat&quot;</span><span class='hljl-p'>,</span><span class='hljl-s'>&quot;Fatality&quot;</span><span class='hljl-p'>);</span><span class='hljl-t'>

 </span><span class='hljl-nf'>violin</span><span class='hljl-p'>(</span><span class='hljl-n'>d</span><span class='hljl-oB'>.</span><span class='hljl-n'>Year</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>d</span><span class='hljl-oB'>.</span><span class='hljl-n'>Perinc</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>color</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-sc'>:gray</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-nf'>boxplot!</span><span class='hljl-p'>(</span><span class='hljl-n'>d</span><span class='hljl-oB'>.</span><span class='hljl-n'>Year</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>d</span><span class='hljl-oB'>.</span><span class='hljl-n'>Perinc</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>color</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-sc'>:black</span><span class='hljl-p'>)</span><span class='hljl-t'>


</span>
</pre>

```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="http://simondanisch.github.io/ReferenceImages/gallery/violin_and_box_plot/media/image.jpg" alt="">

    </p>
</div>

```
