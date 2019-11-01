## Test heatmap + image overlap

```@raw html
<pre class='hljl'>
<span class='hljl-k'>using</span><span class='hljl-t'> </span><span class='hljl-n'>Makie</span><span class='hljl-t'>

 </span><span class='hljl-nf'>heatmap</span><span class='hljl-p'>(</span><span class='hljl-nf'>rand</span><span class='hljl-p'>(</span><span class='hljl-ni'>32</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>32</span><span class='hljl-p'>))</span><span class='hljl-t'>
 </span><span class='hljl-nf'>image!</span><span class='hljl-p'>(</span><span class='hljl-nf'>map</span><span class='hljl-p'>(</span><span class='hljl-n'>x</span><span class='hljl-oB'>-&gt;</span><span class='hljl-nf'>RGBAf0</span><span class='hljl-p'>(</span><span class='hljl-n'>x</span><span class='hljl-p'>,</span><span class='hljl-nfB'>0.5</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-nfB'>0.5</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-nfB'>0.8</span><span class='hljl-p'>),</span><span class='hljl-t'> </span><span class='hljl-nf'>rand</span><span class='hljl-p'>(</span><span class='hljl-ni'>32</span><span class='hljl-p'>,</span><span class='hljl-ni'>32</span><span class='hljl-p'>)))</span><span class='hljl-t'>

</span>
</pre>

```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="http://simondanisch.github.io/ReferenceImages/gallery/test_heatmap___image_overlap/media/image.jpg" alt="">

    </p>
</div>

```
