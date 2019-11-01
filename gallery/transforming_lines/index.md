## Transforming lines

```@raw html
<pre class='hljl'>
<span class='hljl-k'>using</span><span class='hljl-t'> </span><span class='hljl-n'>Makie</span><span class='hljl-t'>

 </span><span class='hljl-n'>N</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-ni'>7</span><span class='hljl-t'> </span><span class='hljl-cs'># number of colours in default palette</span><span class='hljl-t'>
 </span><span class='hljl-n'>sc</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>Scene</span><span class='hljl-p'>()</span><span class='hljl-t'>
 </span><span class='hljl-n'>st</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>Stepper</span><span class='hljl-p'>(</span><span class='hljl-n'>sc</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-s'>&quot;output&quot;</span><span class='hljl-p'>)</span><span class='hljl-t'>

 </span><span class='hljl-n'>xs</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-ni'>0</span><span class='hljl-oB'>:</span><span class='hljl-ni'>9</span><span class='hljl-t'>        </span><span class='hljl-cs'># data</span><span class='hljl-t'>
 </span><span class='hljl-n'>ys</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>zeros</span><span class='hljl-p'>(</span><span class='hljl-ni'>10</span><span class='hljl-p'>)</span><span class='hljl-t'>

 </span><span class='hljl-k'>for</span><span class='hljl-t'> </span><span class='hljl-n'>i</span><span class='hljl-t'> </span><span class='hljl-kp'>in</span><span class='hljl-t'> </span><span class='hljl-ni'>1</span><span class='hljl-oB'>:</span><span class='hljl-n'>N</span><span class='hljl-t'>    </span><span class='hljl-cs'># plot lines</span><span class='hljl-t'>
     </span><span class='hljl-nf'>lines!</span><span class='hljl-p'>(</span><span class='hljl-n'>sc</span><span class='hljl-p'>,</span><span class='hljl-t'>
         </span><span class='hljl-n'>xs</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>ys</span><span class='hljl-p'>;</span><span class='hljl-t'>
         </span><span class='hljl-n'>color</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>AbstractPlotting</span><span class='hljl-oB'>.</span><span class='hljl-n'>default_palettes</span><span class='hljl-oB'>.</span><span class='hljl-n'>color</span><span class='hljl-p'>[][</span><span class='hljl-n'>i</span><span class='hljl-p'>],</span><span class='hljl-t'>
         </span><span class='hljl-n'>limits</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>FRect</span><span class='hljl-p'>((</span><span class='hljl-ni'>0</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>0</span><span class='hljl-p'>),</span><span class='hljl-t'> </span><span class='hljl-p'>(</span><span class='hljl-ni'>10</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>10</span><span class='hljl-p'>)),</span><span class='hljl-t'>
         </span><span class='hljl-n'>linewidth</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-ni'>5</span><span class='hljl-t'>
     </span><span class='hljl-p'>)</span><span class='hljl-t'> </span><span class='hljl-cs'># plot lines with colors</span><span class='hljl-t'>
 </span><span class='hljl-k'>end</span><span class='hljl-t'>

 </span><span class='hljl-nf'>center!</span><span class='hljl-p'>(</span><span class='hljl-n'>sc</span><span class='hljl-p'>)</span><span class='hljl-t'>

 </span><span class='hljl-nf'>step!</span><span class='hljl-p'>(</span><span class='hljl-n'>st</span><span class='hljl-p'>)</span><span class='hljl-t'>

 </span><span class='hljl-k'>for</span><span class='hljl-t'> </span><span class='hljl-p'>(</span><span class='hljl-n'>i</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>rot</span><span class='hljl-p'>)</span><span class='hljl-t'> </span><span class='hljl-kp'>in</span><span class='hljl-t'> </span><span class='hljl-nf'>enumerate</span><span class='hljl-p'>(</span><span class='hljl-nf'>LinRange</span><span class='hljl-p'>(</span><span class='hljl-ni'>0</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>π</span><span class='hljl-oB'>/</span><span class='hljl-ni'>2</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>N</span><span class='hljl-p'>))</span><span class='hljl-t'>
     </span><span class='hljl-nf'>rotate!</span><span class='hljl-p'>(</span><span class='hljl-n'>sc</span><span class='hljl-oB'>.</span><span class='hljl-n'>plots</span><span class='hljl-p'>[</span><span class='hljl-n'>i</span><span class='hljl-oB'>+</span><span class='hljl-ni'>1</span><span class='hljl-p'>],</span><span class='hljl-t'> </span><span class='hljl-n'>rot</span><span class='hljl-p'>)</span><span class='hljl-t'>
     </span><span class='hljl-nf'>arc!</span><span class='hljl-p'>(</span><span class='hljl-n'>sc</span><span class='hljl-p'>,</span><span class='hljl-t'>
         </span><span class='hljl-nf'>Point2f0</span><span class='hljl-p'>(</span><span class='hljl-ni'>0</span><span class='hljl-p'>),</span><span class='hljl-t'>
         </span><span class='hljl-p'>(</span><span class='hljl-ni'>8</span><span class='hljl-t'> </span><span class='hljl-oB'>-</span><span class='hljl-t'> </span><span class='hljl-n'>i</span><span class='hljl-p'>),</span><span class='hljl-t'>
         </span><span class='hljl-n'>pi</span><span class='hljl-oB'>/</span><span class='hljl-ni'>2</span><span class='hljl-p'>,</span><span class='hljl-t'>
         </span><span class='hljl-p'>(</span><span class='hljl-n'>pi</span><span class='hljl-oB'>/</span><span class='hljl-ni'>2</span><span class='hljl-oB'>-</span><span class='hljl-n'>rot</span><span class='hljl-p'>);</span><span class='hljl-t'>
         </span><span class='hljl-n'>color</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>sc</span><span class='hljl-oB'>.</span><span class='hljl-n'>plots</span><span class='hljl-p'>[</span><span class='hljl-n'>i</span><span class='hljl-oB'>+</span><span class='hljl-ni'>1</span><span class='hljl-p'>]</span><span class='hljl-oB'>.</span><span class='hljl-n'>color</span><span class='hljl-p'>,</span><span class='hljl-t'>
         </span><span class='hljl-n'>linewidth</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-ni'>5</span><span class='hljl-p'>,</span><span class='hljl-t'>
         </span><span class='hljl-n'>linestyle</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-sc'>:dash</span><span class='hljl-t'>
     </span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-k'>end</span><span class='hljl-t'>

 </span><span class='hljl-nf'>step!</span><span class='hljl-p'>(</span><span class='hljl-n'>st</span><span class='hljl-p'>)</span><span class='hljl-t'>

</span>
</pre>

```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="http://juliaplots.org/MakieReferenceImages/gallery//transforming_lines/media/image1.jpg" alt="">

    </p>
</div>

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="http://juliaplots.org/MakieReferenceImages/gallery//transforming_lines/media/image2.jpg" alt="">

    </p>
</div>

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="http://juliaplots.org/MakieReferenceImages/gallery//transforming_lines/media/transforming_lines-1.jpg" alt="">

    </p>
</div>

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="http://juliaplots.org/MakieReferenceImages/gallery//transforming_lines/media/transforming_lines-2.jpg" alt="">

    </p>
</div>

```
