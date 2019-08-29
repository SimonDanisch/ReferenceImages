## Hbox

```@raw html
<pre class='hljl'>
<span class='hljl-k'>using</span><span class='hljl-t'> </span><span class='hljl-n'>Makie</span><span class='hljl-t'>

 </span><span class='hljl-n'>t</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>range</span><span class='hljl-p'>(</span><span class='hljl-oB'>-</span><span class='hljl-nfB'>122277.93103448274</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>stop</span><span class='hljl-oB'>=-</span><span class='hljl-nfB'>14798.035304081845</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>length</span><span class='hljl-oB'>=</span><span class='hljl-ni'>29542</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-n'>x</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-oB'>-</span><span class='hljl-ni'>42</span><span class='hljl-t'> </span><span class='hljl-oB'>.-</span><span class='hljl-t'> </span><span class='hljl-nf'>randn</span><span class='hljl-p'>(</span><span class='hljl-nf'>length</span><span class='hljl-p'>(</span><span class='hljl-n'>t</span><span class='hljl-p'>))</span><span class='hljl-t'>
 </span><span class='hljl-n'>sc1</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>scatter</span><span class='hljl-p'>(</span><span class='hljl-n'>t</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>x</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>color</span><span class='hljl-oB'>=:</span><span class='hljl-n'>black</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>markersize</span><span class='hljl-oB'>=</span><span class='hljl-nf'>sqrt</span><span class='hljl-p'>(</span><span class='hljl-nf'>length</span><span class='hljl-p'>(</span><span class='hljl-n'>t</span><span class='hljl-p'>)</span><span class='hljl-oB'>/</span><span class='hljl-ni'>20</span><span class='hljl-p'>))</span><span class='hljl-t'>
 </span><span class='hljl-n'>sc2</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>lines</span><span class='hljl-p'>(</span><span class='hljl-n'>t</span><span class='hljl-p'>[</span><span class='hljl-ni'>1</span><span class='hljl-oB'>:</span><span class='hljl-k'>end</span><span class='hljl-oB'>-</span><span class='hljl-ni'>1</span><span class='hljl-p'>],</span><span class='hljl-t'> </span><span class='hljl-nf'>diff</span><span class='hljl-p'>(</span><span class='hljl-n'>x</span><span class='hljl-p'>),</span><span class='hljl-t'> </span><span class='hljl-n'>color</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-sc'>:blue</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-nf'>hbox</span><span class='hljl-p'>(</span><span class='hljl-n'>sc2</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>sc1</span><span class='hljl-p'>)</span><span class='hljl-t'>

</span>
</pre>

```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="https://simondanisch.github.io/ReferenceImages/gallery/hbox_1/media/image.jpg" alt="">

    </p>
</div>

```
