## timeseries

```@raw html
<pre class='hljl'>
<span class='hljl-k'>using</span><span class='hljl-t'> </span><span class='hljl-n'>Makie</span><span class='hljl-t'>

 </span><span class='hljl-n'>signal</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>Node</span><span class='hljl-p'>(</span><span class='hljl-nfB'>0.0</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-n'>scene</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>timeseries</span><span class='hljl-p'>(</span><span class='hljl-n'>signal</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>history</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-ni'>30</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-nf'>record</span><span class='hljl-p'>(</span><span class='hljl-n'>scene</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-s'>&quot;output.mp4&quot;</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-nf'>LinRange</span><span class='hljl-p'>(</span><span class='hljl-ni'>0</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>10</span><span class='hljl-n'>π</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>240</span><span class='hljl-p'>);</span><span class='hljl-t'> </span><span class='hljl-n'>framerate</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-ni'>24</span><span class='hljl-p'>)</span><span class='hljl-t'> </span><span class='hljl-k'>do</span><span class='hljl-t'> </span><span class='hljl-n'>i</span><span class='hljl-t'>
     </span><span class='hljl-n'>signal</span><span class='hljl-p'>[]</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>sin</span><span class='hljl-p'>(</span><span class='hljl-n'>i</span><span class='hljl-p'>)</span><span class='hljl-t'>
</span><span class='hljl-k'>end</span><span class='hljl-t'>

</span>
</pre>

```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <video controls autoplay loop muted>
  <source src="http://simondanisch.github.io/ReferenceImages/gallery/timeseries_1/media/timeseries_1.mp4" type="video/mp4">
  Your browser does not support mp4. Please use a modern browser like Chrome or Firefox.
</video>

    </p>
</div>

```
