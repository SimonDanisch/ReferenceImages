## Stepper demo

```@raw html
<pre class='hljl'>
<span class='hljl-k'>using</span><span class='hljl-t'> </span><span class='hljl-n'>Makie</span><span class='hljl-t'>

 </span><span class='hljl-k'>function</span><span class='hljl-t'> </span><span class='hljl-nf'>stepper_demo</span><span class='hljl-p'>()</span><span class='hljl-t'>
     </span><span class='hljl-n'>scene</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>Scene</span><span class='hljl-p'>()</span><span class='hljl-t'>
     </span><span class='hljl-n'>pos</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-p'>(</span><span class='hljl-ni'>50</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>50</span><span class='hljl-p'>)</span><span class='hljl-t'>
     </span><span class='hljl-n'>steps</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-p'>[</span><span class='hljl-s'>&quot;Step 1&quot;</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-s'>&quot;Step 2&quot;</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-s'>&quot;Step 3&quot;</span><span class='hljl-p'>]</span><span class='hljl-t'>
     </span><span class='hljl-n'>colors</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>AbstractPlotting</span><span class='hljl-oB'>.</span><span class='hljl-n'>ColorBrewer</span><span class='hljl-oB'>.</span><span class='hljl-nf'>palette</span><span class='hljl-p'>(</span><span class='hljl-s'>&quot;Set1&quot;</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-nf'>length</span><span class='hljl-p'>(</span><span class='hljl-n'>steps</span><span class='hljl-p'>))</span><span class='hljl-t'>
     </span><span class='hljl-nf'>lines!</span><span class='hljl-p'>(</span><span class='hljl-n'>scene</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-nf'>Rect</span><span class='hljl-p'>(</span><span class='hljl-ni'>0</span><span class='hljl-p'>,</span><span class='hljl-ni'>0</span><span class='hljl-p'>,</span><span class='hljl-ni'>500</span><span class='hljl-p'>,</span><span class='hljl-ni'>500</span><span class='hljl-p'>),</span><span class='hljl-t'> </span><span class='hljl-n'>linewidth</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nfB'>0.0001</span><span class='hljl-p'>)</span><span class='hljl-t'>
     </span><span class='hljl-cs'># initialize the stepper and give it an output destination</span><span class='hljl-t'>
     </span><span class='hljl-n'>st</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>Stepper</span><span class='hljl-p'>(</span><span class='hljl-n'>scene</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-s'>&quot;output&quot;</span><span class='hljl-p'>)</span><span class='hljl-t'>

     </span><span class='hljl-k'>for</span><span class='hljl-t'> </span><span class='hljl-n'>i</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-ni'>1</span><span class='hljl-oB'>:</span><span class='hljl-nf'>length</span><span class='hljl-p'>(</span><span class='hljl-n'>steps</span><span class='hljl-p'>)</span><span class='hljl-t'>
         </span><span class='hljl-nf'>text!</span><span class='hljl-p'>(</span><span class='hljl-t'>
             </span><span class='hljl-n'>scene</span><span class='hljl-p'>,</span><span class='hljl-t'>
             </span><span class='hljl-n'>steps</span><span class='hljl-p'>[</span><span class='hljl-n'>i</span><span class='hljl-p'>],</span><span class='hljl-t'>
             </span><span class='hljl-n'>position</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>pos</span><span class='hljl-p'>,</span><span class='hljl-t'>
             </span><span class='hljl-n'>align</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-p'>(</span><span class='hljl-sc'>:left</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-sc'>:bottom</span><span class='hljl-p'>),</span><span class='hljl-t'>
             </span><span class='hljl-n'>textsize</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-ni'>100</span><span class='hljl-p'>,</span><span class='hljl-t'>
             </span><span class='hljl-n'>font</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-s'>&quot;Blackchancery&quot;</span><span class='hljl-p'>,</span><span class='hljl-t'>
             </span><span class='hljl-n'>color</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>colors</span><span class='hljl-p'>[</span><span class='hljl-n'>i</span><span class='hljl-p'>],</span><span class='hljl-t'>
             </span><span class='hljl-n'>scale_plot</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-kc'>false</span><span class='hljl-t'>
         </span><span class='hljl-p'>)</span><span class='hljl-t'>
         </span><span class='hljl-n'>pos</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>pos</span><span class='hljl-t'> </span><span class='hljl-oB'>.+</span><span class='hljl-t'> </span><span class='hljl-ni'>100</span><span class='hljl-t'>
         </span><span class='hljl-nf'>step!</span><span class='hljl-p'>(</span><span class='hljl-n'>st</span><span class='hljl-p'>)</span><span class='hljl-t'> </span><span class='hljl-cs'># saves the step and increments the step by one</span><span class='hljl-t'>
     </span><span class='hljl-k'>end</span><span class='hljl-t'>
     </span><span class='hljl-n'>st</span><span class='hljl-t'>
 </span><span class='hljl-k'>end</span><span class='hljl-t'>
 </span><span class='hljl-nf'>stepper_demo</span><span class='hljl-p'>()</span><span class='hljl-t'>

</span>
</pre>

```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="http://juliaplots.org/MakieReferenceImages/gallery//stepper_demo/media/stepper_demo-1.jpg" alt="">

    </p>
</div>

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="http://juliaplots.org/MakieReferenceImages/gallery//stepper_demo/media/stepper_demo-2.jpg" alt="">

    </p>
</div>

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="http://juliaplots.org/MakieReferenceImages/gallery//stepper_demo/media/stepper_demo-3.jpg" alt="">

    </p>
</div>

```
