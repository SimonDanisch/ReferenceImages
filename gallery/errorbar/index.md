## Errorbar

```@raw html
<pre class='hljl'>
<span class='hljl-k'>using</span><span class='hljl-t'> </span><span class='hljl-n'>Makie</span><span class='hljl-t'>
 </span><span class='hljl-k'>using</span><span class='hljl-t'> </span><span class='hljl-n'>StatsMakie</span><span class='hljl-t'>

 </span><span class='hljl-n'>x</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-p'>[</span><span class='hljl-ni'>1</span><span class='hljl-oB'>:</span><span class='hljl-ni'>4</span><span class='hljl-p'>;]</span><span class='hljl-t'>
 </span><span class='hljl-n'>y</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'>  </span><span class='hljl-p'>[</span><span class='hljl-ni'>1</span><span class='hljl-oB'>:</span><span class='hljl-ni'>4</span><span class='hljl-p'>;]</span><span class='hljl-t'>
 </span><span class='hljl-n'>Δx</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>fill</span><span class='hljl-p'>(</span><span class='hljl-nfB'>0.25</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>4</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-n'>Δy</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>fill</span><span class='hljl-p'>(</span><span class='hljl-nfB'>0.25</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>4</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-n'>p</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>errorbar</span><span class='hljl-p'>(</span><span class='hljl-n'>x</span><span class='hljl-p'>,</span><span class='hljl-n'>y</span><span class='hljl-p'>,</span><span class='hljl-n'>Δx</span><span class='hljl-p'>,</span><span class='hljl-n'>Δy</span><span class='hljl-p'>,</span><span class='hljl-n'>xcolor</span><span class='hljl-oB'>=:</span><span class='hljl-n'>green</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>ycolor</span><span class='hljl-oB'>=:</span><span class='hljl-n'>red</span><span class='hljl-p'>)</span><span class='hljl-t'>

</span>
</pre>

```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="http://juliaplots.org/MakieReferenceImages/gallery//errorbar/media/image.jpg" alt="">

    </p>
</div>

```
