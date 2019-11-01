## pulsing marker

```@raw html
<pre class='hljl'>
<span class='hljl-k'>using</span><span class='hljl-t'> </span><span class='hljl-n'>Makie</span><span class='hljl-t'>

 </span><span class='hljl-n'>N</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-ni'>100</span><span class='hljl-t'>
 </span><span class='hljl-n'>scene</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>scatter</span><span class='hljl-p'>([</span><span class='hljl-ni'>0</span><span class='hljl-p'>],</span><span class='hljl-t'> </span><span class='hljl-p'>[</span><span class='hljl-ni'>0</span><span class='hljl-p'>],</span><span class='hljl-t'> </span><span class='hljl-n'>marker</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-sc'>&#39;❤&#39;</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>markersize</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nfB'>0.5</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>color</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-sc'>:red</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>raw</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-kc'>true</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-n'>s</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>scene</span><span class='hljl-p'>[</span><span class='hljl-k'>end</span><span class='hljl-p'>]</span><span class='hljl-t'> </span><span class='hljl-cs'># last plot in scene</span><span class='hljl-t'>
 </span><span class='hljl-nf'>record</span><span class='hljl-p'>(</span><span class='hljl-n'>scene</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-s'>&quot;output.mp4&quot;</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-nf'>range</span><span class='hljl-p'>(</span><span class='hljl-ni'>0</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>stop</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-ni'>10</span><span class='hljl-n'>pi</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>length</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>N</span><span class='hljl-p'>))</span><span class='hljl-t'> </span><span class='hljl-k'>do</span><span class='hljl-t'> </span><span class='hljl-n'>i</span><span class='hljl-t'>
     </span><span class='hljl-n'>s</span><span class='hljl-p'>[</span><span class='hljl-sc'>:markersize</span><span class='hljl-p'>]</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-p'>(</span><span class='hljl-nf'>cos</span><span class='hljl-p'>(</span><span class='hljl-n'>i</span><span class='hljl-p'>)</span><span class='hljl-t'> </span><span class='hljl-oB'>+</span><span class='hljl-t'> </span><span class='hljl-ni'>1</span><span class='hljl-p'>)</span><span class='hljl-t'> </span><span class='hljl-oB'>/</span><span class='hljl-t'> </span><span class='hljl-ni'>4</span><span class='hljl-t'> </span><span class='hljl-oB'>+</span><span class='hljl-t'> </span><span class='hljl-nfB'>0.2</span><span class='hljl-t'>
</span><span class='hljl-k'>end</span><span class='hljl-t'>

</span>
</pre>

```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <video controls autoplay loop muted>
  <source src="http://simondanisch.github.io/ReferenceImages/gallery/pulsing_marker/media/pulsing_marker.mp4" type="video/mp4">
  Your browser does not support mp4. Please use a modern browser like Chrome or Firefox.
</video>

    </p>
</div>

```
