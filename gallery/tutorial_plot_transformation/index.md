## Tutorial plot transformation

```@raw html
<pre class='hljl'>
<span class='hljl-k'>using</span><span class='hljl-t'> </span><span class='hljl-n'>Makie</span><span class='hljl-t'>

 </span><span class='hljl-n'>data</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>rand</span><span class='hljl-p'>(</span><span class='hljl-ni'>10</span><span class='hljl-p'>)</span><span class='hljl-t'>

 </span><span class='hljl-n'>scene</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>Scene</span><span class='hljl-p'>()</span><span class='hljl-t'>
 </span><span class='hljl-n'>st</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>Stepper</span><span class='hljl-p'>(</span><span class='hljl-n'>scene</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-s'>&quot;output&quot;</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-n'>lineplot</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>lines!</span><span class='hljl-p'>(</span><span class='hljl-n'>scene</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>data</span><span class='hljl-p'>)[</span><span class='hljl-k'>end</span><span class='hljl-p'>]</span><span class='hljl-t'>    </span><span class='hljl-cs'># gets the last defined plot for the Scene</span><span class='hljl-t'>
 </span><span class='hljl-n'>scatplot</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>scatter!</span><span class='hljl-p'>(</span><span class='hljl-n'>scene</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>data</span><span class='hljl-p'>)[</span><span class='hljl-k'>end</span><span class='hljl-p'>]</span><span class='hljl-t'>  </span><span class='hljl-cs'># same thing but the last defined plot is scatter</span><span class='hljl-t'>
 </span><span class='hljl-nf'>step!</span><span class='hljl-p'>(</span><span class='hljl-n'>st</span><span class='hljl-p'>)</span><span class='hljl-t'>

 </span><span class='hljl-nf'>rotate!</span><span class='hljl-p'>(</span><span class='hljl-n'>lineplot</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-nfB'>0.025</span><span class='hljl-n'>π</span><span class='hljl-p'>)</span><span class='hljl-t'> </span><span class='hljl-cs'># only the lines are rotated, not the scatter</span><span class='hljl-t'>
 </span><span class='hljl-nf'>step!</span><span class='hljl-p'>(</span><span class='hljl-n'>st</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-n'>st</span><span class='hljl-t'>

</span>
</pre>

```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="http://juliaplots.org/MakieReferenceImages/gallery//tutorial_plot_transformation/media/tutorial_plot_transformation-1.jpg" alt="">

    </p>
</div>

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="http://juliaplots.org/MakieReferenceImages/gallery//tutorial_plot_transformation/media/tutorial_plot_transformation-2.jpg" alt="">

    </p>
</div>

```
