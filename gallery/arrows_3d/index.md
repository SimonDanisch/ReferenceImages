## Arrows 3D

```@raw html
<pre class='hljl'>
<span class='hljl-k'>using</span><span class='hljl-t'> </span><span class='hljl-n'>Makie</span><span class='hljl-t'>
 </span><span class='hljl-k'>using</span><span class='hljl-t'> </span><span class='hljl-n'>LinearAlgebra</span><span class='hljl-t'>

 </span><span class='hljl-k'>function</span><span class='hljl-t'> </span><span class='hljl-nf'>SphericalToCartesian</span><span class='hljl-p'>(</span><span class='hljl-n'>r</span><span class='hljl-oB'>::</span><span class='hljl-n'>T</span><span class='hljl-p'>,</span><span class='hljl-n'>θ</span><span class='hljl-oB'>::</span><span class='hljl-n'>T</span><span class='hljl-p'>,</span><span class='hljl-n'>ϕ</span><span class='hljl-oB'>::</span><span class='hljl-n'>T</span><span class='hljl-p'>)</span><span class='hljl-t'> </span><span class='hljl-n'>where</span><span class='hljl-t'> </span><span class='hljl-n'>T</span><span class='hljl-oB'>&lt;:</span><span class='hljl-n'>AbstractArray</span><span class='hljl-t'>
     </span><span class='hljl-n'>x</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> @</span><span class='hljl-oB'>.</span><span class='hljl-n'>r</span><span class='hljl-oB'>*</span><span class='hljl-nf'>sin</span><span class='hljl-p'>(</span><span class='hljl-n'>θ</span><span class='hljl-p'>)</span><span class='hljl-oB'>*</span><span class='hljl-nf'>cos</span><span class='hljl-p'>(</span><span class='hljl-n'>ϕ</span><span class='hljl-p'>)</span><span class='hljl-t'>
     </span><span class='hljl-n'>y</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> @</span><span class='hljl-oB'>.</span><span class='hljl-n'>r</span><span class='hljl-oB'>*</span><span class='hljl-nf'>sin</span><span class='hljl-p'>(</span><span class='hljl-n'>θ</span><span class='hljl-p'>)</span><span class='hljl-oB'>*</span><span class='hljl-nf'>sin</span><span class='hljl-p'>(</span><span class='hljl-n'>ϕ</span><span class='hljl-p'>)</span><span class='hljl-t'>
     </span><span class='hljl-n'>z</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> @</span><span class='hljl-oB'>.</span><span class='hljl-n'>r</span><span class='hljl-oB'>*</span><span class='hljl-nf'>cos</span><span class='hljl-p'>(</span><span class='hljl-n'>θ</span><span class='hljl-p'>)</span><span class='hljl-t'>
     </span><span class='hljl-n'>Point3f0</span><span class='hljl-oB'>.</span><span class='hljl-p'>(</span><span class='hljl-n'>x</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>y</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>z</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-k'>end</span><span class='hljl-t'>
 </span><span class='hljl-n'>n</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-ni'>100</span><span class='hljl-oB'>^</span><span class='hljl-ni'>2</span><span class='hljl-t'> </span><span class='hljl-cs'>#number of points to generate</span><span class='hljl-t'>
 </span><span class='hljl-n'>r</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>ones</span><span class='hljl-p'>(</span><span class='hljl-n'>n</span><span class='hljl-p'>);</span><span class='hljl-t'>
 </span><span class='hljl-n'>θ</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>acos</span><span class='hljl-oB'>.</span><span class='hljl-p'>(</span><span class='hljl-ni'>1</span><span class='hljl-t'> </span><span class='hljl-oB'>.-</span><span class='hljl-t'> </span><span class='hljl-ni'>2</span><span class='hljl-t'> </span><span class='hljl-oB'>.*</span><span class='hljl-t'> </span><span class='hljl-nf'>rand</span><span class='hljl-p'>(</span><span class='hljl-n'>n</span><span class='hljl-p'>))</span><span class='hljl-t'>
 </span><span class='hljl-n'>φ</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-ni'>2</span><span class='hljl-n'>π</span><span class='hljl-t'> </span><span class='hljl-oB'>*</span><span class='hljl-t'> </span><span class='hljl-nf'>rand</span><span class='hljl-p'>(</span><span class='hljl-n'>n</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-n'>pts</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>SphericalToCartesian</span><span class='hljl-p'>(</span><span class='hljl-n'>r</span><span class='hljl-p'>,</span><span class='hljl-n'>θ</span><span class='hljl-p'>,</span><span class='hljl-n'>φ</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-nf'>arrows</span><span class='hljl-p'>(</span><span class='hljl-n'>pts</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-p'>(</span><span class='hljl-n'>normalize</span><span class='hljl-oB'>.</span><span class='hljl-p'>(</span><span class='hljl-n'>pts</span><span class='hljl-p'>)</span><span class='hljl-t'> </span><span class='hljl-oB'>.*</span><span class='hljl-t'> </span><span class='hljl-nfB'>0.1f0</span><span class='hljl-p'>),</span><span class='hljl-t'> </span><span class='hljl-n'>arrowsize</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nfB'>0.02</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>linecolor</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-sc'>:green</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>arrowcolor</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-sc'>:darkblue</span><span class='hljl-p'>)</span><span class='hljl-t'>

</span>
</pre>

```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="https://simondanisch.github.io/ReferenceImages/gallery/arrows_3d/media/image.jpg" alt="">

    </p>
</div>

```
