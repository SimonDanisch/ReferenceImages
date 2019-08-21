## Marker sizes + Marker colors

```@raw html
<pre class='hljl'>
<span class='hljl-k'>using</span><span class='hljl-t'> </span><span class='hljl-n'>Makie</span><span class='hljl-t'>

 </span><span class='hljl-nf'>scatter</span><span class='hljl-p'>(</span><span class='hljl-t'>
     </span><span class='hljl-nf'>rand</span><span class='hljl-p'>(</span><span class='hljl-ni'>20</span><span class='hljl-p'>),</span><span class='hljl-t'> </span><span class='hljl-nf'>rand</span><span class='hljl-p'>(</span><span class='hljl-ni'>20</span><span class='hljl-p'>),</span><span class='hljl-t'>
     </span><span class='hljl-n'>markersize</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>rand</span><span class='hljl-p'>(</span><span class='hljl-ni'>20</span><span class='hljl-p'>)</span><span class='hljl-t'> </span><span class='hljl-oB'>./</span><span class='hljl-ni'>20</span><span class='hljl-t'> </span><span class='hljl-oB'>.+</span><span class='hljl-t'> </span><span class='hljl-nfB'>0.02</span><span class='hljl-p'>,</span><span class='hljl-t'>
     </span><span class='hljl-n'>color</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>rand</span><span class='hljl-p'>(</span><span class='hljl-n'>RGBf0</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>20</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-p'>)</span><span class='hljl-t'>

</span>
</pre>

```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="http://juliaplots.org/MakieReferenceImages/gallery//marker_sizes___marker_colors/media/image.jpg" alt="">

    </p>
</div>

```
