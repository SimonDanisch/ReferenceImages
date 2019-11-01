## poly and colormap

```@raw html
<pre class='hljl'>
<span class='hljl-k'>using</span><span class='hljl-t'> </span><span class='hljl-n'>Makie</span><span class='hljl-t'>

 </span><span class='hljl-n'>points</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>Point2f0</span><span class='hljl-p'>[[</span><span class='hljl-nfB'>0.0</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-nfB'>0.0</span><span class='hljl-p'>],</span><span class='hljl-t'> </span><span class='hljl-p'>[</span><span class='hljl-nfB'>0.1</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-nfB'>0.0</span><span class='hljl-p'>],</span><span class='hljl-t'> </span><span class='hljl-p'>[</span><span class='hljl-nfB'>0.1</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-nfB'>0.1</span><span class='hljl-p'>],</span><span class='hljl-t'> </span><span class='hljl-p'>[</span><span class='hljl-nfB'>0.0</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-nfB'>0.1</span><span class='hljl-p'>]]</span><span class='hljl-t'>
 </span><span class='hljl-n'>colors</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-p'>[</span><span class='hljl-nfB'>0.0</span><span class='hljl-t'> </span><span class='hljl-p'>,</span><span class='hljl-nfB'>0.0</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-nfB'>0.5</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-nfB'>0.0</span><span class='hljl-p'>]</span><span class='hljl-t'>
 </span><span class='hljl-n'>scene</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>poly</span><span class='hljl-p'>(</span><span class='hljl-n'>points</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>color</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>colors</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>colorrange</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-p'>(</span><span class='hljl-nfB'>0.0</span><span class='hljl-p'>,</span><span class='hljl-nfB'>1.0</span><span class='hljl-p'>))</span><span class='hljl-t'>
 </span><span class='hljl-n'>points</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>Point2f0</span><span class='hljl-p'>[[</span><span class='hljl-nfB'>0.1</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-nfB'>0.1</span><span class='hljl-p'>],</span><span class='hljl-t'> </span><span class='hljl-p'>[</span><span class='hljl-nfB'>0.2</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-nfB'>0.1</span><span class='hljl-p'>],</span><span class='hljl-t'> </span><span class='hljl-p'>[</span><span class='hljl-nfB'>0.2</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-nfB'>0.2</span><span class='hljl-p'>],</span><span class='hljl-t'> </span><span class='hljl-p'>[</span><span class='hljl-nfB'>0.1</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-nfB'>0.2</span><span class='hljl-p'>]]</span><span class='hljl-t'>
 </span><span class='hljl-n'>colors</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-p'>[</span><span class='hljl-nfB'>0.5</span><span class='hljl-p'>,</span><span class='hljl-nfB'>0.5</span><span class='hljl-p'>,</span><span class='hljl-nfB'>1.0</span><span class='hljl-p'>,</span><span class='hljl-nfB'>0.3</span><span class='hljl-p'>]</span><span class='hljl-t'>
 </span><span class='hljl-nf'>poly!</span><span class='hljl-p'>(</span><span class='hljl-n'>scene</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>points</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>color</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>colors</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>colorrange</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-p'>(</span><span class='hljl-nfB'>0.0</span><span class='hljl-p'>,</span><span class='hljl-nfB'>1.0</span><span class='hljl-p'>))</span><span class='hljl-t'>
 </span><span class='hljl-n'>scene</span><span class='hljl-t'>

</span>
</pre>

```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="http://simondanisch.github.io/ReferenceImages/gallery/poly_and_colormap/media/image.jpg" alt="">

    </p>
</div>

```
