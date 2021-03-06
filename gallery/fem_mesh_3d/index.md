## FEM mesh 3D

```@raw html
<pre class='hljl'>
<span class='hljl-k'>using</span><span class='hljl-t'> </span><span class='hljl-n'>Makie</span><span class='hljl-t'>
 </span><span class='hljl-k'>using</span><span class='hljl-t'> </span><span class='hljl-n'>GeometryTypes</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>GLMakie</span><span class='hljl-t'>

 </span><span class='hljl-n'>cat</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>GLMakie</span><span class='hljl-oB'>.</span><span class='hljl-nf'>loadasset</span><span class='hljl-p'>(</span><span class='hljl-s'>&quot;cat.obj&quot;</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-n'>vertices</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>decompose</span><span class='hljl-p'>(</span><span class='hljl-n'>Point3f0</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>cat</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-n'>faces</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>decompose</span><span class='hljl-p'>(</span><span class='hljl-nf'>Face</span><span class='hljl-p'>{</span><span class='hljl-ni'>3</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>Int</span><span class='hljl-p'>},</span><span class='hljl-t'> </span><span class='hljl-n'>cat</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-n'>coordinates</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-p'>[</span><span class='hljl-n'>vertices</span><span class='hljl-p'>[</span><span class='hljl-n'>i</span><span class='hljl-p'>][</span><span class='hljl-n'>j</span><span class='hljl-p'>]</span><span class='hljl-t'> </span><span class='hljl-k'>for</span><span class='hljl-t'> </span><span class='hljl-n'>i</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-ni'>1</span><span class='hljl-oB'>:</span><span class='hljl-nf'>length</span><span class='hljl-p'>(</span><span class='hljl-n'>vertices</span><span class='hljl-p'>),</span><span class='hljl-t'> </span><span class='hljl-n'>j</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-ni'>1</span><span class='hljl-oB'>:</span><span class='hljl-ni'>3</span><span class='hljl-p'>]</span><span class='hljl-t'>
 </span><span class='hljl-n'>connectivity</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-p'>[</span><span class='hljl-n'>faces</span><span class='hljl-p'>[</span><span class='hljl-n'>i</span><span class='hljl-p'>][</span><span class='hljl-n'>j</span><span class='hljl-p'>]</span><span class='hljl-t'> </span><span class='hljl-k'>for</span><span class='hljl-t'> </span><span class='hljl-n'>i</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-ni'>1</span><span class='hljl-oB'>:</span><span class='hljl-nf'>length</span><span class='hljl-p'>(</span><span class='hljl-n'>faces</span><span class='hljl-p'>),</span><span class='hljl-t'> </span><span class='hljl-n'>j</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-ni'>1</span><span class='hljl-oB'>:</span><span class='hljl-ni'>3</span><span class='hljl-p'>]</span><span class='hljl-t'>
 </span><span class='hljl-nf'>mesh</span><span class='hljl-p'>(</span><span class='hljl-t'>
     </span><span class='hljl-n'>coordinates</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>connectivity</span><span class='hljl-p'>,</span><span class='hljl-t'>
     </span><span class='hljl-n'>color</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>rand</span><span class='hljl-p'>(</span><span class='hljl-nf'>length</span><span class='hljl-p'>(</span><span class='hljl-n'>vertices</span><span class='hljl-p'>))</span><span class='hljl-t'>
 </span><span class='hljl-p'>)</span><span class='hljl-t'>

</span>
</pre>

```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="http://simondanisch.github.io/ReferenceImages/gallery/fem_mesh_3d/media/image.jpg" alt="">

    </p>
</div>

```
