## Marker offset

```@raw html
<pre class='hljl'>
<span class='hljl-k'>using</span><span class='hljl-t'> </span><span class='hljl-n'>Makie</span><span class='hljl-t'>

 </span><span class='hljl-n'>scene</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>Scene</span><span class='hljl-p'>()</span><span class='hljl-t'>
 </span><span class='hljl-n'>points</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>Point2f0</span><span class='hljl-p'>[(</span><span class='hljl-ni'>0</span><span class='hljl-p'>,</span><span class='hljl-ni'>0</span><span class='hljl-p'>),</span><span class='hljl-t'> </span><span class='hljl-p'>(</span><span class='hljl-ni'>1</span><span class='hljl-p'>,</span><span class='hljl-ni'>1</span><span class='hljl-p'>),</span><span class='hljl-t'> </span><span class='hljl-p'>(</span><span class='hljl-ni'>2</span><span class='hljl-p'>,</span><span class='hljl-ni'>2</span><span class='hljl-p'>)]</span><span class='hljl-t'>
 </span><span class='hljl-n'>offset</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>rand</span><span class='hljl-p'>(</span><span class='hljl-n'>Point2f0</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>3</span><span class='hljl-p'>)</span><span class='hljl-oB'>./</span><span class='hljl-ni'>5</span><span class='hljl-t'>
 </span><span class='hljl-nf'>scatter!</span><span class='hljl-p'>(</span><span class='hljl-n'>scene</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>points</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-nf'>scatter!</span><span class='hljl-p'>(</span><span class='hljl-n'>scene</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>points</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>marker_offset</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>offset</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>color</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-sc'>:red</span><span class='hljl-p'>)</span><span class='hljl-t'>

</span>
</pre>

```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="https://simondanisch.github.io/ReferenceImages/gallery/marker_offset/media/image.jpg" alt="">

    </p>
</div>

```
