## Tutorial basic theming

```@raw html
<pre class='hljl'>
<span class='hljl-k'>using</span><span class='hljl-t'> </span><span class='hljl-n'>Makie</span><span class='hljl-t'>

 </span><span class='hljl-n'>x</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>range</span><span class='hljl-p'>(</span><span class='hljl-ni'>0</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>stop</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-ni'>2</span><span class='hljl-n'>pi</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>length</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-ni'>40</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-nf'>f</span><span class='hljl-p'>(</span><span class='hljl-n'>x</span><span class='hljl-p'>)</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>cos</span><span class='hljl-oB'>.</span><span class='hljl-p'>(</span><span class='hljl-n'>x</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-n'>y</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>f</span><span class='hljl-p'>(</span><span class='hljl-n'>x</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-n'>scene</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>lines</span><span class='hljl-p'>(</span><span class='hljl-n'>x</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>y</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>color</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-sc'>:blue</span><span class='hljl-p'>)</span><span class='hljl-t'>

 </span><span class='hljl-n'>axis</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>scene</span><span class='hljl-p'>[</span><span class='hljl-n'>Axis</span><span class='hljl-p'>]</span><span class='hljl-t'> </span><span class='hljl-cs'># get the axis object from the scene</span><span class='hljl-t'>
 </span><span class='hljl-n'>axis</span><span class='hljl-oB'>.</span><span class='hljl-n'>grid</span><span class='hljl-oB'>.</span><span class='hljl-n'>linecolor</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-p'>((</span><span class='hljl-sc'>:red</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-nfB'>0.5</span><span class='hljl-p'>),</span><span class='hljl-t'> </span><span class='hljl-p'>(</span><span class='hljl-sc'>:blue</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-nfB'>0.5</span><span class='hljl-p'>))</span><span class='hljl-t'>
 </span><span class='hljl-n'>axis</span><span class='hljl-oB'>.</span><span class='hljl-n'>names</span><span class='hljl-oB'>.</span><span class='hljl-n'>textcolor</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-p'>((</span><span class='hljl-sc'>:red</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-nfB'>1.0</span><span class='hljl-p'>),</span><span class='hljl-t'> </span><span class='hljl-p'>(</span><span class='hljl-sc'>:blue</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-nfB'>1.0</span><span class='hljl-p'>))</span><span class='hljl-t'>
 </span><span class='hljl-n'>axis</span><span class='hljl-oB'>.</span><span class='hljl-n'>names</span><span class='hljl-oB'>.</span><span class='hljl-n'>axisnames</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-p'>(</span><span class='hljl-s'>&quot;x&quot;</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-s'>&quot;y = cos(x)&quot;</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-n'>scene</span><span class='hljl-t'>

</span>
</pre>

```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="https://simondanisch.github.io/ReferenceImages/gallery/tutorial_basic_theming/media/image.jpg" alt="">

    </p>
</div>

```
