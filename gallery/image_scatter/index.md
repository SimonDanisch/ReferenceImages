## image scatter

```@raw html
<pre class='hljl'>
<span class='hljl-k'>using</span><span class='hljl-t'> </span><span class='hljl-n'>Makie</span><span class='hljl-t'>
 </span><span class='hljl-k'>using</span><span class='hljl-t'> </span><span class='hljl-n'>LinearAlgebra</span><span class='hljl-t'>

 </span><span class='hljl-nf'>scatter</span><span class='hljl-p'>(</span><span class='hljl-t'>
     </span><span class='hljl-ni'>1</span><span class='hljl-oB'>:</span><span class='hljl-ni'>10</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>1</span><span class='hljl-oB'>:</span><span class='hljl-ni'>10</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-nf'>rand</span><span class='hljl-p'>(</span><span class='hljl-ni'>10</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>10</span><span class='hljl-p'>)</span><span class='hljl-t'> </span><span class='hljl-oB'>.*</span><span class='hljl-t'> </span><span class='hljl-ni'>10</span><span class='hljl-p'>,</span><span class='hljl-t'>
     </span><span class='hljl-n'>rotations</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>normalize</span><span class='hljl-oB'>.</span><span class='hljl-p'>(</span><span class='hljl-nf'>rand</span><span class='hljl-p'>(</span><span class='hljl-n'>Quaternionf0</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>10</span><span class='hljl-oB'>*</span><span class='hljl-ni'>10</span><span class='hljl-p'>)),</span><span class='hljl-t'>
     </span><span class='hljl-n'>markersize</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-ni'>1</span><span class='hljl-p'>,</span><span class='hljl-t'>
     </span><span class='hljl-cs'># can also be an array of images for each point</span><span class='hljl-t'>
     </span><span class='hljl-cs'># need to be the same size for best performance, though</span><span class='hljl-t'>
     </span><span class='hljl-n'>marker</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>AbstractPlotting</span><span class='hljl-oB'>.</span><span class='hljl-nf'>logo</span><span class='hljl-p'>()</span><span class='hljl-t'>
 </span><span class='hljl-p'>)</span><span class='hljl-t'>

</span>
</pre>

```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="https://simondanisch.github.io/ReferenceImages/gallery/image_scatter/media/image.jpg" alt="">

    </p>
</div>

```
