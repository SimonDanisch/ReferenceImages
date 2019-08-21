## colormaps

```@raw html
<pre class='hljl'>
<span class='hljl-k'>using</span><span class='hljl-t'> </span><span class='hljl-n'>Makie</span><span class='hljl-t'>

 </span><span class='hljl-n'>h</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nfB'>0.0</span><span class='hljl-t'>
 </span><span class='hljl-n'>offset</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nfB'>0.1</span><span class='hljl-t'>
 </span><span class='hljl-n'>scene</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>Scene</span><span class='hljl-p'>()</span><span class='hljl-t'>
 </span><span class='hljl-nf'>cam2d!</span><span class='hljl-p'>(</span><span class='hljl-n'>scene</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-n'>plot</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>map</span><span class='hljl-p'>(</span><span class='hljl-nf'>collect</span><span class='hljl-p'>(</span><span class='hljl-n'>AbstractPlotting</span><span class='hljl-oB'>.</span><span class='hljl-n'>all_gradient_names</span><span class='hljl-p'>))</span><span class='hljl-t'> </span><span class='hljl-k'>do</span><span class='hljl-t'> </span><span class='hljl-n'>cmap</span><span class='hljl-t'>
     </span><span class='hljl-kd'>global</span><span class='hljl-t'> </span><span class='hljl-n'>h</span><span class='hljl-t'>
     </span><span class='hljl-n'>c</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>to_colormap</span><span class='hljl-p'>(</span><span class='hljl-n'>cmap</span><span class='hljl-p'>)</span><span class='hljl-t'>
     </span><span class='hljl-n'>cbar</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>image!</span><span class='hljl-p'>(</span><span class='hljl-t'>
         </span><span class='hljl-n'>scene</span><span class='hljl-p'>,</span><span class='hljl-t'>
         </span><span class='hljl-nf'>range</span><span class='hljl-p'>(</span><span class='hljl-ni'>0</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>stop</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-ni'>10</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>length</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>length</span><span class='hljl-p'>(</span><span class='hljl-n'>c</span><span class='hljl-p'>)),</span><span class='hljl-t'>
         </span><span class='hljl-nf'>range</span><span class='hljl-p'>(</span><span class='hljl-ni'>0</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>stop</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-ni'>1</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>length</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>length</span><span class='hljl-p'>(</span><span class='hljl-n'>c</span><span class='hljl-p'>)),</span><span class='hljl-t'>
         </span><span class='hljl-nf'>reshape</span><span class='hljl-p'>(</span><span class='hljl-n'>c</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-p'>(</span><span class='hljl-nf'>length</span><span class='hljl-p'>(</span><span class='hljl-n'>c</span><span class='hljl-p'>),</span><span class='hljl-ni'>1</span><span class='hljl-p'>)),</span><span class='hljl-t'>
         </span><span class='hljl-n'>show_axis</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-kc'>false</span><span class='hljl-t'>
     </span><span class='hljl-p'>)[</span><span class='hljl-k'>end</span><span class='hljl-p'>]</span><span class='hljl-t'>
     </span><span class='hljl-nf'>text!</span><span class='hljl-p'>(</span><span class='hljl-t'>
         </span><span class='hljl-n'>scene</span><span class='hljl-p'>,</span><span class='hljl-t'>
         </span><span class='hljl-nf'>string</span><span class='hljl-p'>(</span><span class='hljl-n'>cmap</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-s'>&quot;:&quot;</span><span class='hljl-p'>),</span><span class='hljl-t'>
         </span><span class='hljl-n'>position</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>Point2f0</span><span class='hljl-p'>(</span><span class='hljl-oB'>-</span><span class='hljl-nfB'>0.1</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-nfB'>0.5</span><span class='hljl-t'> </span><span class='hljl-oB'>+</span><span class='hljl-t'> </span><span class='hljl-n'>h</span><span class='hljl-p'>),</span><span class='hljl-t'>
         </span><span class='hljl-n'>align</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-p'>(</span><span class='hljl-sc'>:right</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-sc'>:center</span><span class='hljl-p'>),</span><span class='hljl-t'>
         </span><span class='hljl-n'>show_axis</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-kc'>false</span><span class='hljl-p'>,</span><span class='hljl-t'>
         </span><span class='hljl-n'>textsize</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-ni'>1</span><span class='hljl-t'>
     </span><span class='hljl-p'>)</span><span class='hljl-t'>
     </span><span class='hljl-nf'>translate!</span><span class='hljl-p'>(</span><span class='hljl-n'>cbar</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>0</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>h</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>0</span><span class='hljl-p'>)</span><span class='hljl-t'>
     </span><span class='hljl-n'>h</span><span class='hljl-t'> </span><span class='hljl-oB'>-=</span><span class='hljl-t'> </span><span class='hljl-p'>(</span><span class='hljl-ni'>1</span><span class='hljl-t'> </span><span class='hljl-oB'>+</span><span class='hljl-t'> </span><span class='hljl-n'>offset</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-k'>end</span><span class='hljl-t'>
 </span><span class='hljl-n'>scene</span><span class='hljl-t'>

</span>
</pre>

```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="http://juliaplots.org/MakieReferenceImages/gallery//colormaps/media/image.jpg" alt="">

    </p>
</div>

```
