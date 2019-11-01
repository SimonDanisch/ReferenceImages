## Merged color Mesh

```@raw html
<pre class='hljl'>
<span class='hljl-k'>using</span><span class='hljl-t'> </span><span class='hljl-n'>Makie</span><span class='hljl-t'>
 </span><span class='hljl-k'>using</span><span class='hljl-t'> </span><span class='hljl-n'>GeometryTypes</span><span class='hljl-t'>

 </span><span class='hljl-n'>x</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>Vec3f0</span><span class='hljl-p'>(</span><span class='hljl-ni'>0</span><span class='hljl-p'>);</span><span class='hljl-t'> </span><span class='hljl-n'>baselen</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nfB'>0.2f0</span><span class='hljl-p'>;</span><span class='hljl-t'> </span><span class='hljl-n'>dirlen</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nfB'>1f0</span><span class='hljl-t'>
 </span><span class='hljl-cs'># create an array of differently colored boxes in the direction of the 3 axes</span><span class='hljl-t'>
 </span><span class='hljl-n'>rectangles</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-p'>[</span><span class='hljl-t'>
     </span><span class='hljl-p'>(</span><span class='hljl-nf'>HyperRectangle</span><span class='hljl-p'>(</span><span class='hljl-nf'>Vec3f0</span><span class='hljl-p'>(</span><span class='hljl-n'>x</span><span class='hljl-p'>),</span><span class='hljl-t'> </span><span class='hljl-nf'>Vec3f0</span><span class='hljl-p'>(</span><span class='hljl-n'>dirlen</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>baselen</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>baselen</span><span class='hljl-p'>)),</span><span class='hljl-t'> </span><span class='hljl-nf'>RGBAf0</span><span class='hljl-p'>(</span><span class='hljl-ni'>1</span><span class='hljl-p'>,</span><span class='hljl-ni'>0</span><span class='hljl-p'>,</span><span class='hljl-ni'>0</span><span class='hljl-p'>,</span><span class='hljl-ni'>1</span><span class='hljl-p'>)),</span><span class='hljl-t'>
     </span><span class='hljl-p'>(</span><span class='hljl-nf'>HyperRectangle</span><span class='hljl-p'>(</span><span class='hljl-nf'>Vec3f0</span><span class='hljl-p'>(</span><span class='hljl-n'>x</span><span class='hljl-p'>),</span><span class='hljl-t'> </span><span class='hljl-nf'>Vec3f0</span><span class='hljl-p'>(</span><span class='hljl-n'>baselen</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>dirlen</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>baselen</span><span class='hljl-p'>)),</span><span class='hljl-t'> </span><span class='hljl-nf'>RGBAf0</span><span class='hljl-p'>(</span><span class='hljl-ni'>0</span><span class='hljl-p'>,</span><span class='hljl-ni'>1</span><span class='hljl-p'>,</span><span class='hljl-ni'>0</span><span class='hljl-p'>,</span><span class='hljl-ni'>1</span><span class='hljl-p'>)),</span><span class='hljl-t'>
     </span><span class='hljl-p'>(</span><span class='hljl-nf'>HyperRectangle</span><span class='hljl-p'>(</span><span class='hljl-nf'>Vec3f0</span><span class='hljl-p'>(</span><span class='hljl-n'>x</span><span class='hljl-p'>),</span><span class='hljl-t'> </span><span class='hljl-nf'>Vec3f0</span><span class='hljl-p'>(</span><span class='hljl-n'>baselen</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>baselen</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>dirlen</span><span class='hljl-p'>)),</span><span class='hljl-t'> </span><span class='hljl-nf'>RGBAf0</span><span class='hljl-p'>(</span><span class='hljl-ni'>0</span><span class='hljl-p'>,</span><span class='hljl-ni'>0</span><span class='hljl-p'>,</span><span class='hljl-ni'>1</span><span class='hljl-p'>,</span><span class='hljl-ni'>1</span><span class='hljl-p'>))</span><span class='hljl-t'>
 </span><span class='hljl-p'>]</span><span class='hljl-t'>
 </span><span class='hljl-n'>meshes</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>map</span><span class='hljl-p'>(</span><span class='hljl-n'>GLNormalMesh</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>rectangles</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-nf'>mesh</span><span class='hljl-p'>(</span><span class='hljl-nf'>merge</span><span class='hljl-p'>(</span><span class='hljl-n'>meshes</span><span class='hljl-p'>))</span><span class='hljl-t'>

</span>
</pre>

```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="http://simondanisch.github.io/ReferenceImages/gallery/merged_color_mesh/media/image.jpg" alt="">

    </p>
</div>

```
