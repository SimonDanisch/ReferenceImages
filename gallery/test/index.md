## Test

```@raw html
<pre class='hljl'>
<span class='hljl-k'>using</span><span class='hljl-t'> </span><span class='hljl-n'>Makie</span><span class='hljl-t'>

 </span><span class='hljl-n'>scene</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>Scene</span><span class='hljl-p'>(</span><span class='hljl-n'>raw</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-kc'>true</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>camera</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>campixel!</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-nf'>text!</span><span class='hljl-p'>(</span><span class='hljl-t'>
     </span><span class='hljl-n'>scene</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-s'>&quot;boundingbox&quot;</span><span class='hljl-p'>,</span><span class='hljl-t'>
     </span><span class='hljl-n'>align</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-p'>(</span><span class='hljl-sc'>:left</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-sc'>:center</span><span class='hljl-p'>),</span><span class='hljl-t'>
     </span><span class='hljl-n'>position</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-p'>(</span><span class='hljl-ni'>50</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>50</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-nf'>scale!</span><span class='hljl-p'>(</span><span class='hljl-n'>scene</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-nf'>Vec3f0</span><span class='hljl-p'>(</span><span class='hljl-ni'>4</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>1</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>1</span><span class='hljl-p'>))</span><span class='hljl-t'>
 </span><span class='hljl-nf'>linesegments!</span><span class='hljl-p'>(</span><span class='hljl-nf'>boundingbox</span><span class='hljl-p'>(</span><span class='hljl-n'>scene</span><span class='hljl-p'>))</span><span class='hljl-t'>
 </span><span class='hljl-n'>offset</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-ni'>0</span><span class='hljl-t'>
 </span><span class='hljl-k'>for</span><span class='hljl-t'> </span><span class='hljl-n'>a_lign</span><span class='hljl-t'> </span><span class='hljl-kp'>in</span><span class='hljl-t'> </span><span class='hljl-p'>(</span><span class='hljl-sc'>:center</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-sc'>:left</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-sc'>:right</span><span class='hljl-p'>),</span><span class='hljl-t'> </span><span class='hljl-n'>b_lign</span><span class='hljl-t'> </span><span class='hljl-kp'>in</span><span class='hljl-t'> </span><span class='hljl-p'>(</span><span class='hljl-sc'>:center</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-sc'>:left</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-sc'>:right</span><span class='hljl-p'>)</span><span class='hljl-t'>
     </span><span class='hljl-kd'>global</span><span class='hljl-t'> </span><span class='hljl-n'>offset</span><span class='hljl-t'>
     </span><span class='hljl-n'>t</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>text!</span><span class='hljl-p'>(</span><span class='hljl-t'>
         </span><span class='hljl-s'>&quot;boundingbox&quot;</span><span class='hljl-p'>,</span><span class='hljl-t'>
         </span><span class='hljl-n'>align</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-p'>(</span><span class='hljl-n'>a_lign</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>b_lign</span><span class='hljl-p'>),</span><span class='hljl-t'>
         </span><span class='hljl-n'>position</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-p'>(</span><span class='hljl-ni'>50</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>100</span><span class='hljl-t'> </span><span class='hljl-oB'>+</span><span class='hljl-t'> </span><span class='hljl-n'>offset</span><span class='hljl-p'>)</span><span class='hljl-t'>
     </span><span class='hljl-p'>)[</span><span class='hljl-k'>end</span><span class='hljl-p'>]</span><span class='hljl-t'>
     </span><span class='hljl-nf'>linesegments!</span><span class='hljl-p'>(</span><span class='hljl-nf'>boundingbox</span><span class='hljl-p'>(</span><span class='hljl-n'>t</span><span class='hljl-p'>))</span><span class='hljl-t'>
     </span><span class='hljl-n'>offset</span><span class='hljl-t'> </span><span class='hljl-oB'>+=</span><span class='hljl-t'> </span><span class='hljl-ni'>50</span><span class='hljl-t'>
 </span><span class='hljl-k'>end</span><span class='hljl-t'>
 </span><span class='hljl-n'>scene</span><span class='hljl-t'>

</span>
</pre>

```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="http://juliaplots.org/MakieReferenceImages/gallery//test/media/image.jpg" alt="">

    </p>
</div>

```
