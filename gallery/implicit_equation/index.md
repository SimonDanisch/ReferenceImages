## Implicit equation

```@raw html
<pre class='hljl'>
<span class='hljl-k'>using</span><span class='hljl-t'> </span><span class='hljl-n'>Makie</span><span class='hljl-t'>

 </span><span class='hljl-n'>r</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>range</span><span class='hljl-p'>(</span><span class='hljl-oB'>-</span><span class='hljl-ni'>5</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>stop</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-ni'>5</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>length</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-ni'>400</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-p'>(</span><span class='hljl-n'>a</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>b</span><span class='hljl-p'>)</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-oB'>-</span><span class='hljl-ni'>1</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>2</span><span class='hljl-t'>
 </span><span class='hljl-n'>z</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-p'>((</span><span class='hljl-n'>x</span><span class='hljl-p'>,</span><span class='hljl-n'>y</span><span class='hljl-p'>)</span><span class='hljl-t'> </span><span class='hljl-oB'>-&gt;</span><span class='hljl-t'> </span><span class='hljl-n'>y</span><span class='hljl-oB'>.^</span><span class='hljl-ni'>4</span><span class='hljl-t'> </span><span class='hljl-oB'>-</span><span class='hljl-t'> </span><span class='hljl-n'>x</span><span class='hljl-oB'>.^</span><span class='hljl-ni'>4</span><span class='hljl-t'> </span><span class='hljl-oB'>+</span><span class='hljl-t'> </span><span class='hljl-n'>a</span><span class='hljl-t'> </span><span class='hljl-oB'>.*</span><span class='hljl-t'> </span><span class='hljl-n'>y</span><span class='hljl-oB'>.^</span><span class='hljl-ni'>2</span><span class='hljl-t'> </span><span class='hljl-oB'>+</span><span class='hljl-t'> </span><span class='hljl-n'>b</span><span class='hljl-t'> </span><span class='hljl-oB'>.*</span><span class='hljl-t'> </span><span class='hljl-n'>x</span><span class='hljl-oB'>.^</span><span class='hljl-ni'>2</span><span class='hljl-p'>)</span><span class='hljl-oB'>.</span><span class='hljl-p'>(</span><span class='hljl-n'>r</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>r</span><span class='hljl-oB'>&#39;</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-n'>z2</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'>  </span><span class='hljl-n'>z</span><span class='hljl-t'> </span><span class='hljl-oB'>.*</span><span class='hljl-t'> </span><span class='hljl-p'>(</span><span class='hljl-n'>abs</span><span class='hljl-oB'>.</span><span class='hljl-p'>(</span><span class='hljl-n'>z</span><span class='hljl-p'>)</span><span class='hljl-t'> </span><span class='hljl-oB'>.&lt;</span><span class='hljl-t'> </span><span class='hljl-ni'>250</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-nf'>contour</span><span class='hljl-p'>(</span><span class='hljl-n'>r</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>r</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>z2</span><span class='hljl-p'>)</span><span class='hljl-t'>

</span>
</pre>

```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="http://juliaplots.org/MakieReferenceImages/gallery//implicit_equation/media/image.jpg" alt="">

    </p>
</div>

```
