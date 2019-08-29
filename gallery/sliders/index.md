## sliders

```@raw html
<pre class='hljl'>
<span class='hljl-k'>using</span><span class='hljl-t'> </span><span class='hljl-n'>Makie</span><span class='hljl-t'>

 </span><span class='hljl-n'>s1</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>slider</span><span class='hljl-p'>(</span><span class='hljl-nf'>LinRange</span><span class='hljl-p'>(</span><span class='hljl-nfB'>0.01</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>1</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>100</span><span class='hljl-p'>),</span><span class='hljl-t'> </span><span class='hljl-n'>raw</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-kc'>true</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>camera</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>campixel!</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>start</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nfB'>0.3</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-n'>s2</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>slider</span><span class='hljl-p'>(</span><span class='hljl-nf'>LinRange</span><span class='hljl-p'>(</span><span class='hljl-oB'>-</span><span class='hljl-ni'>2</span><span class='hljl-n'>pi</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>2</span><span class='hljl-n'>pi</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>100</span><span class='hljl-p'>),</span><span class='hljl-t'> </span><span class='hljl-n'>raw</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-kc'>true</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>camera</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>campixel!</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-n'>data</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>lift</span><span class='hljl-p'>(</span><span class='hljl-n'>s2</span><span class='hljl-p'>[</span><span class='hljl-k'>end</span><span class='hljl-p'>][</span><span class='hljl-sc'>:value</span><span class='hljl-p'>])</span><span class='hljl-t'> </span><span class='hljl-k'>do</span><span class='hljl-t'> </span><span class='hljl-n'>v</span><span class='hljl-t'>
     </span><span class='hljl-nf'>map</span><span class='hljl-p'>(</span><span class='hljl-nf'>LinRange</span><span class='hljl-p'>(</span><span class='hljl-ni'>0</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>2</span><span class='hljl-n'>pi</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>100</span><span class='hljl-p'>))</span><span class='hljl-t'> </span><span class='hljl-k'>do</span><span class='hljl-t'> </span><span class='hljl-n'>x</span><span class='hljl-t'>
         </span><span class='hljl-nfB'>4f0</span><span class='hljl-t'> </span><span class='hljl-oB'>.*</span><span class='hljl-t'> </span><span class='hljl-nf'>Point2f0</span><span class='hljl-p'>(</span><span class='hljl-nf'>sin</span><span class='hljl-p'>(</span><span class='hljl-n'>x</span><span class='hljl-p'>)</span><span class='hljl-t'> </span><span class='hljl-oB'>+</span><span class='hljl-t'> </span><span class='hljl-p'>(</span><span class='hljl-nf'>sin</span><span class='hljl-p'>(</span><span class='hljl-n'>x</span><span class='hljl-t'> </span><span class='hljl-oB'>*</span><span class='hljl-t'> </span><span class='hljl-n'>v</span><span class='hljl-p'>)</span><span class='hljl-t'> </span><span class='hljl-oB'>.*</span><span class='hljl-t'> </span><span class='hljl-nfB'>0.1</span><span class='hljl-p'>),</span><span class='hljl-t'> </span><span class='hljl-nf'>cos</span><span class='hljl-p'>(</span><span class='hljl-n'>x</span><span class='hljl-p'>)</span><span class='hljl-t'> </span><span class='hljl-oB'>+</span><span class='hljl-t'> </span><span class='hljl-p'>(</span><span class='hljl-nf'>cos</span><span class='hljl-p'>(</span><span class='hljl-n'>x</span><span class='hljl-t'> </span><span class='hljl-oB'>*</span><span class='hljl-t'> </span><span class='hljl-n'>v</span><span class='hljl-p'>)</span><span class='hljl-t'> </span><span class='hljl-oB'>.*</span><span class='hljl-t'> </span><span class='hljl-nfB'>0.1</span><span class='hljl-p'>))</span><span class='hljl-t'>
     </span><span class='hljl-k'>end</span><span class='hljl-t'>
 </span><span class='hljl-k'>end</span><span class='hljl-t'>
 </span><span class='hljl-n'>p</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>scatter</span><span class='hljl-p'>(</span><span class='hljl-n'>data</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>markersize</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>s1</span><span class='hljl-p'>[</span><span class='hljl-k'>end</span><span class='hljl-p'>][</span><span class='hljl-sc'>:value</span><span class='hljl-p'>])</span><span class='hljl-t'>

 </span><span class='hljl-nf'>RecordEvents</span><span class='hljl-p'>(</span><span class='hljl-t'>
     </span><span class='hljl-nf'>hbox</span><span class='hljl-p'>(</span><span class='hljl-n'>p</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-nf'>vbox</span><span class='hljl-p'>(</span><span class='hljl-n'>s1</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>s2</span><span class='hljl-p'>),</span><span class='hljl-t'> </span><span class='hljl-n'>parent</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>Scene</span><span class='hljl-p'>(</span><span class='hljl-n'>resolution</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-p'>(</span><span class='hljl-ni'>500</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>500</span><span class='hljl-p'>))),</span><span class='hljl-t'>
     </span><span class='hljl-s'>&quot;output&quot;</span><span class='hljl-t'>
 </span><span class='hljl-p'>)</span><span class='hljl-t'>

</span>
</pre>

```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <video controls autoplay loop muted>
  <source src="https://simondanisch.github.io/ReferenceImages/gallery/sliders/media/video.mp4" type="video/mp4">
  Your browser does not support mp4. Please use a modern browser like Chrome or Firefox.
</video>

    </p>
</div>

```
