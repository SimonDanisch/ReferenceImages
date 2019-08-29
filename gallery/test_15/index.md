## Test

```@raw html
<pre class='hljl'>
<span class='hljl-k'>using</span><span class='hljl-t'> </span><span class='hljl-n'>Makie</span><span class='hljl-t'>
 </span><span class='hljl-k'>using</span><span class='hljl-t'> </span><span class='hljl-n'>GeometryTypes</span><span class='hljl-t'>

 </span><span class='hljl-n'>s1</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>GLNormalUVMesh</span><span class='hljl-p'>(</span><span class='hljl-nf'>Sphere</span><span class='hljl-p'>(</span><span class='hljl-nf'>Point3f0</span><span class='hljl-p'>(</span><span class='hljl-ni'>0</span><span class='hljl-p'>),</span><span class='hljl-t'> </span><span class='hljl-nfB'>1f0</span><span class='hljl-p'>))</span><span class='hljl-t'>
 </span><span class='hljl-nf'>mesh</span><span class='hljl-p'>(</span><span class='hljl-nf'>GLNormalUVMesh</span><span class='hljl-p'>(</span><span class='hljl-nf'>Sphere</span><span class='hljl-p'>(</span><span class='hljl-nf'>Point3f0</span><span class='hljl-p'>(</span><span class='hljl-ni'>0</span><span class='hljl-p'>),</span><span class='hljl-t'> </span><span class='hljl-nfB'>1f0</span><span class='hljl-p'>)),</span><span class='hljl-t'> </span><span class='hljl-n'>color</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>rand</span><span class='hljl-p'>(</span><span class='hljl-ni'>50</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>50</span><span class='hljl-p'>))</span><span class='hljl-t'>
 </span><span class='hljl-cs'># ugh, bug In GeometryTypes for UVs of non unit spheres.</span><span class='hljl-t'>
 </span><span class='hljl-n'>s2</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>GLNormalUVMesh</span><span class='hljl-p'>(</span><span class='hljl-nf'>Sphere</span><span class='hljl-p'>(</span><span class='hljl-nf'>Point3f0</span><span class='hljl-p'>(</span><span class='hljl-ni'>0</span><span class='hljl-p'>),</span><span class='hljl-t'> </span><span class='hljl-nfB'>1f0</span><span class='hljl-p'>))</span><span class='hljl-t'>
 </span><span class='hljl-n'>s2</span><span class='hljl-oB'>.</span><span class='hljl-n'>vertices</span><span class='hljl-t'> </span><span class='hljl-oB'>.=</span><span class='hljl-t'> </span><span class='hljl-n'>s2</span><span class='hljl-oB'>.</span><span class='hljl-n'>vertices</span><span class='hljl-t'> </span><span class='hljl-oB'>.+</span><span class='hljl-t'> </span><span class='hljl-p'>(</span><span class='hljl-nf'>Point3f0</span><span class='hljl-p'>(</span><span class='hljl-ni'>0</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>2</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>0</span><span class='hljl-p'>),)</span><span class='hljl-t'>
 </span><span class='hljl-nf'>mesh!</span><span class='hljl-p'>(</span><span class='hljl-n'>s2</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>color</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>rand</span><span class='hljl-p'>(</span><span class='hljl-n'>RGBAf0</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>50</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>50</span><span class='hljl-p'>))</span><span class='hljl-t'>

</span>
</pre>

```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="https://simondanisch.github.io/ReferenceImages/gallery/test_15/media/image.jpg" alt="">

    </p>
</div>

```
