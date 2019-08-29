## Stars

```@raw html
<pre class='hljl'>
<span class='hljl-k'>using</span><span class='hljl-t'> </span><span class='hljl-n'>Makie</span><span class='hljl-t'>

 </span><span class='hljl-n'>stars</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-ni'>100_000</span><span class='hljl-t'>
 </span><span class='hljl-n'>scene</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>Scene</span><span class='hljl-p'>(</span><span class='hljl-n'>backgroundcolor</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-sc'>:black</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-nf'>scatter!</span><span class='hljl-p'>(</span><span class='hljl-t'>
     </span><span class='hljl-n'>scene</span><span class='hljl-p'>,</span><span class='hljl-t'>
     </span><span class='hljl-p'>(</span><span class='hljl-nf'>randn</span><span class='hljl-p'>(</span><span class='hljl-n'>Point3f0</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>stars</span><span class='hljl-p'>)</span><span class='hljl-t'> </span><span class='hljl-oB'>.-</span><span class='hljl-t'> </span><span class='hljl-nfB'>0.5</span><span class='hljl-p'>)</span><span class='hljl-t'> </span><span class='hljl-oB'>.*</span><span class='hljl-t'> </span><span class='hljl-ni'>10</span><span class='hljl-p'>,</span><span class='hljl-t'>
     </span><span class='hljl-n'>glowwidth</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-ni'>1</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>glowcolor</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-p'>(</span><span class='hljl-sc'>:white</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-nfB'>0.1</span><span class='hljl-p'>),</span><span class='hljl-t'> </span><span class='hljl-n'>color</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>rand</span><span class='hljl-p'>(</span><span class='hljl-n'>stars</span><span class='hljl-p'>),</span><span class='hljl-t'>
     </span><span class='hljl-n'>colormap</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-p'>[(</span><span class='hljl-sc'>:white</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-nfB'>0.4</span><span class='hljl-p'>),</span><span class='hljl-t'> </span><span class='hljl-p'>(</span><span class='hljl-sc'>:blue</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-nfB'>0.4</span><span class='hljl-p'>),</span><span class='hljl-t'> </span><span class='hljl-p'>(</span><span class='hljl-sc'>:yellow</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-nfB'>0.4</span><span class='hljl-p'>)],</span><span class='hljl-t'>
     </span><span class='hljl-n'>markersize</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>rand</span><span class='hljl-p'>(</span><span class='hljl-nf'>range</span><span class='hljl-p'>(</span><span class='hljl-nfB'>0.0001</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>stop</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nfB'>0.05</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>length</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-ni'>100</span><span class='hljl-p'>),</span><span class='hljl-t'> </span><span class='hljl-n'>stars</span><span class='hljl-p'>),</span><span class='hljl-t'>
     </span><span class='hljl-n'>show_axis</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-kc'>false</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>transparency</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-kc'>true</span><span class='hljl-t'>
 </span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-nf'>update_cam!</span><span class='hljl-p'>(</span><span class='hljl-n'>scene</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-nf'>FRect3D</span><span class='hljl-p'>(</span><span class='hljl-nf'>Vec3f0</span><span class='hljl-p'>(</span><span class='hljl-oB'>-</span><span class='hljl-ni'>5</span><span class='hljl-p'>),</span><span class='hljl-t'> </span><span class='hljl-nf'>Vec3f0</span><span class='hljl-p'>(</span><span class='hljl-ni'>10</span><span class='hljl-p'>)))</span><span class='hljl-t'>
 </span><span class='hljl-n'>scene</span><span class='hljl-oB'>.</span><span class='hljl-n'>center</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-kc'>false</span><span class='hljl-t'>
 </span><span class='hljl-n'>scene</span><span class='hljl-t'>

</span>
</pre>

```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="https://simondanisch.github.io/ReferenceImages/gallery/stars/media/image.jpg" alt="">

    </p>
</div>

```
