## Textured Mesh

```@raw html
<pre class='hljl'>
<span class='hljl-k'>using</span><span class='hljl-t'> </span><span class='hljl-n'>Makie</span><span class='hljl-t'>
 </span><span class='hljl-k'>using</span><span class='hljl-t'> </span><span class='hljl-n'>FileIO</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>GLMakie</span><span class='hljl-t'>

 </span><span class='hljl-n'>scene</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>Scene</span><span class='hljl-p'>(</span><span class='hljl-n'>resolution</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-p'>(</span><span class='hljl-ni'>500</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>500</span><span class='hljl-p'>))</span><span class='hljl-t'>
 </span><span class='hljl-n'>catmesh</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>FileIO</span><span class='hljl-oB'>.</span><span class='hljl-nf'>load</span><span class='hljl-p'>(</span><span class='hljl-n'>GLMakie</span><span class='hljl-oB'>.</span><span class='hljl-nf'>assetpath</span><span class='hljl-p'>(</span><span class='hljl-s'>&quot;cat.obj&quot;</span><span class='hljl-p'>),</span><span class='hljl-t'> </span><span class='hljl-n'>GLNormalUVMesh</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-nf'>mesh</span><span class='hljl-p'>(</span><span class='hljl-n'>catmesh</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>color</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>GLMakie</span><span class='hljl-oB'>.</span><span class='hljl-nf'>loadasset</span><span class='hljl-p'>(</span><span class='hljl-s'>&quot;diffusemap.tga&quot;</span><span class='hljl-p'>))</span><span class='hljl-t'>

</span>
</pre>

```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="http://simondanisch.github.io/ReferenceImages/gallery/textured_mesh/media/image.jpg" alt="">

    </p>
</div>

```
