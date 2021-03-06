## Comparing contours, image, surfaces and heatmaps

```@raw html
<pre class='hljl'>
<span class='hljl-k'>using</span><span class='hljl-t'> </span><span class='hljl-n'>Makie</span><span class='hljl-t'>

 </span><span class='hljl-n'>N</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-ni'>20</span><span class='hljl-t'>
 </span><span class='hljl-n'>x</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>LinRange</span><span class='hljl-p'>(</span><span class='hljl-oB'>-</span><span class='hljl-nfB'>0.3</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>1</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>N</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-n'>y</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>LinRange</span><span class='hljl-p'>(</span><span class='hljl-oB'>-</span><span class='hljl-ni'>1</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-nfB'>0.5</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>N</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-n'>z</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>x</span><span class='hljl-t'> </span><span class='hljl-oB'>.*</span><span class='hljl-t'> </span><span class='hljl-n'>y</span><span class='hljl-oB'>&#39;</span><span class='hljl-t'>
 </span><span class='hljl-nf'>hbox</span><span class='hljl-p'>(</span><span class='hljl-t'>
     </span><span class='hljl-nf'>vbox</span><span class='hljl-p'>(</span><span class='hljl-t'>
         </span><span class='hljl-nf'>contour</span><span class='hljl-p'>(</span><span class='hljl-n'>x</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>y</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>z</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>levels</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-ni'>20</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>linewidth</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-ni'>3</span><span class='hljl-p'>),</span><span class='hljl-t'>
         </span><span class='hljl-nf'>contour</span><span class='hljl-p'>(</span><span class='hljl-n'>x</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>y</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>z</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>levels</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-ni'>0</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>linewidth</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-ni'>0</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>fillrange</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-kc'>true</span><span class='hljl-p'>),</span><span class='hljl-t'>
         </span><span class='hljl-nf'>heatmap</span><span class='hljl-p'>(</span><span class='hljl-n'>x</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>y</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>z</span><span class='hljl-p'>),</span><span class='hljl-t'>
     </span><span class='hljl-p'>),</span><span class='hljl-t'>
     </span><span class='hljl-nf'>vbox</span><span class='hljl-p'>(</span><span class='hljl-t'>
         </span><span class='hljl-nf'>image</span><span class='hljl-p'>(</span><span class='hljl-n'>x</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>y</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>z</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>colormap</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-sc'>:viridis</span><span class='hljl-p'>),</span><span class='hljl-t'>
         </span><span class='hljl-nf'>surface</span><span class='hljl-p'>(</span><span class='hljl-n'>x</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>y</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-nf'>fill</span><span class='hljl-p'>(</span><span class='hljl-nfB'>0f0</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>N</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>N</span><span class='hljl-p'>),</span><span class='hljl-t'> </span><span class='hljl-n'>color</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>z</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>shading</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-kc'>false</span><span class='hljl-p'>),</span><span class='hljl-t'>
         </span><span class='hljl-nf'>image</span><span class='hljl-p'>(</span><span class='hljl-oB'>-</span><span class='hljl-nfB'>0.3</span><span class='hljl-oB'>..</span><span class='hljl-ni'>1</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-oB'>-</span><span class='hljl-nfB'>1..0.5</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>AbstractPlotting</span><span class='hljl-oB'>.</span><span class='hljl-nf'>logo</span><span class='hljl-p'>())</span><span class='hljl-t'>
     </span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-p'>)</span><span class='hljl-t'>

</span>
</pre>

```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="http://simondanisch.github.io/ReferenceImages/gallery/comparing_contours,_image,_surfaces_and_heatmaps/media/image.jpg" alt="">

    </p>
</div>

```
