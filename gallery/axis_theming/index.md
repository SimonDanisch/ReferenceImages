## Axis theming

```@raw html
<pre class='hljl'>
<span class='hljl-k'>using</span><span class='hljl-t'> </span><span class='hljl-n'>Makie</span><span class='hljl-t'>
 </span><span class='hljl-k'>using</span><span class='hljl-t'> </span><span class='hljl-n'>GeometryTypes</span><span class='hljl-t'>

 </span><span class='hljl-n'>scene</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>Scene</span><span class='hljl-p'>()</span><span class='hljl-t'>
 </span><span class='hljl-n'>points</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>decompose</span><span class='hljl-p'>(</span><span class='hljl-n'>Point2f0</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-nf'>Circle</span><span class='hljl-p'>(</span><span class='hljl-nf'>Point2f0</span><span class='hljl-p'>(</span><span class='hljl-ni'>10</span><span class='hljl-p'>),</span><span class='hljl-t'> </span><span class='hljl-nfB'>10f0</span><span class='hljl-p'>),</span><span class='hljl-t'> </span><span class='hljl-ni'>9</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-nf'>lines!</span><span class='hljl-p'>(</span><span class='hljl-t'>
     </span><span class='hljl-n'>scene</span><span class='hljl-p'>,</span><span class='hljl-t'>
     </span><span class='hljl-n'>points</span><span class='hljl-p'>,</span><span class='hljl-t'>
     </span><span class='hljl-n'>linewidth</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-ni'>8</span><span class='hljl-p'>,</span><span class='hljl-t'>
     </span><span class='hljl-n'>color</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-sc'>:black</span><span class='hljl-t'>
 </span><span class='hljl-p'>)</span><span class='hljl-t'>

 </span><span class='hljl-n'>axis</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>scene</span><span class='hljl-p'>[</span><span class='hljl-n'>Axis</span><span class='hljl-p'>]</span><span class='hljl-t'> </span><span class='hljl-cs'># get axis</span><span class='hljl-t'>
 </span><span class='hljl-n'>scene</span><span class='hljl-t'>

 </span><span class='hljl-n'>st</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>Stepper</span><span class='hljl-p'>(</span><span class='hljl-n'>scene</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-s'>&quot;output&quot;</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-nf'>step!</span><span class='hljl-p'>(</span><span class='hljl-n'>st</span><span class='hljl-p'>);</span><span class='hljl-t'>
 </span><span class='hljl-n'>axis</span><span class='hljl-p'>[</span><span class='hljl-sc'>:frame</span><span class='hljl-p'>][</span><span class='hljl-sc'>:linewidth</span><span class='hljl-p'>]</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-ni'>5</span><span class='hljl-t'>
 </span><span class='hljl-nf'>step!</span><span class='hljl-p'>(</span><span class='hljl-n'>st</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-n'>axis</span><span class='hljl-p'>[</span><span class='hljl-sc'>:grid</span><span class='hljl-p'>][</span><span class='hljl-sc'>:linewidth</span><span class='hljl-p'>]</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-p'>(</span><span class='hljl-ni'>1</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>5</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-nf'>step!</span><span class='hljl-p'>(</span><span class='hljl-n'>st</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-n'>axis</span><span class='hljl-p'>[</span><span class='hljl-sc'>:grid</span><span class='hljl-p'>][</span><span class='hljl-sc'>:linecolor</span><span class='hljl-p'>]</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-p'>((</span><span class='hljl-sc'>:red</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-nfB'>0.3</span><span class='hljl-p'>),</span><span class='hljl-t'> </span><span class='hljl-p'>(</span><span class='hljl-sc'>:blue</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-nfB'>0.5</span><span class='hljl-p'>))</span><span class='hljl-t'>
 </span><span class='hljl-nf'>step!</span><span class='hljl-p'>(</span><span class='hljl-n'>st</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-n'>axis</span><span class='hljl-p'>[</span><span class='hljl-sc'>:names</span><span class='hljl-p'>][</span><span class='hljl-sc'>:axisnames</span><span class='hljl-p'>]</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-p'>(</span><span class='hljl-s'>&quot;x&quot;</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-s'>&quot;y   &quot;</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-nf'>step!</span><span class='hljl-p'>(</span><span class='hljl-n'>st</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-n'>axis</span><span class='hljl-p'>[</span><span class='hljl-sc'>:ticks</span><span class='hljl-p'>][</span><span class='hljl-sc'>:title_gap</span><span class='hljl-p'>]</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-ni'>1</span><span class='hljl-t'>
 </span><span class='hljl-nf'>step!</span><span class='hljl-p'>(</span><span class='hljl-n'>st</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-n'>axis</span><span class='hljl-p'>[</span><span class='hljl-sc'>:names</span><span class='hljl-p'>][</span><span class='hljl-sc'>:rotation</span><span class='hljl-p'>]</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-p'>(</span><span class='hljl-nfB'>0.0</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-oB'>-</span><span class='hljl-ni'>3</span><span class='hljl-oB'>/</span><span class='hljl-ni'>8</span><span class='hljl-oB'>*</span><span class='hljl-n'>pi</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-nf'>step!</span><span class='hljl-p'>(</span><span class='hljl-n'>st</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-n'>axis</span><span class='hljl-p'>[</span><span class='hljl-sc'>:names</span><span class='hljl-p'>][</span><span class='hljl-sc'>:textcolor</span><span class='hljl-p'>]</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-p'>((</span><span class='hljl-sc'>:red</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-nfB'>1.0</span><span class='hljl-p'>),</span><span class='hljl-t'> </span><span class='hljl-p'>(</span><span class='hljl-sc'>:blue</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-nfB'>1.0</span><span class='hljl-p'>))</span><span class='hljl-t'>
 </span><span class='hljl-nf'>step!</span><span class='hljl-p'>(</span><span class='hljl-n'>st</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-n'>axis</span><span class='hljl-p'>[</span><span class='hljl-sc'>:ticks</span><span class='hljl-p'>][</span><span class='hljl-sc'>:font</span><span class='hljl-p'>]</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-p'>(</span><span class='hljl-s'>&quot;Dejavu Sans&quot;</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-s'>&quot;Helvetica&quot;</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-nf'>step!</span><span class='hljl-p'>(</span><span class='hljl-n'>st</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-n'>axis</span><span class='hljl-p'>[</span><span class='hljl-sc'>:ticks</span><span class='hljl-p'>][</span><span class='hljl-sc'>:rotation</span><span class='hljl-p'>]</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-p'>(</span><span class='hljl-nfB'>0.0</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-oB'>-</span><span class='hljl-n'>pi</span><span class='hljl-oB'>/</span><span class='hljl-ni'>2</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-nf'>step!</span><span class='hljl-p'>(</span><span class='hljl-n'>st</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-n'>axis</span><span class='hljl-p'>[</span><span class='hljl-sc'>:ticks</span><span class='hljl-p'>][</span><span class='hljl-sc'>:textsize</span><span class='hljl-p'>]</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-p'>(</span><span class='hljl-ni'>3</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>7</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-nf'>step!</span><span class='hljl-p'>(</span><span class='hljl-n'>st</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-n'>axis</span><span class='hljl-p'>[</span><span class='hljl-sc'>:ticks</span><span class='hljl-p'>][</span><span class='hljl-sc'>:gap</span><span class='hljl-p'>]</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-ni'>5</span><span class='hljl-t'>
 </span><span class='hljl-nf'>step!</span><span class='hljl-p'>(</span><span class='hljl-n'>st</span><span class='hljl-p'>)</span><span class='hljl-t'>

</span>
</pre>

```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="https://simondanisch.github.io/ReferenceImages/gallery/axis_theming/media/axis_theming-1.jpg" alt="">

    </p>
</div>

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="https://simondanisch.github.io/ReferenceImages/gallery/axis_theming/media/axis_theming-10.jpg" alt="">

    </p>
</div>

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="https://simondanisch.github.io/ReferenceImages/gallery/axis_theming/media/axis_theming-11.jpg" alt="">

    </p>
</div>

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="https://simondanisch.github.io/ReferenceImages/gallery/axis_theming/media/axis_theming-12.jpg" alt="">

    </p>
</div>

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="https://simondanisch.github.io/ReferenceImages/gallery/axis_theming/media/axis_theming-2.jpg" alt="">

    </p>
</div>

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="https://simondanisch.github.io/ReferenceImages/gallery/axis_theming/media/axis_theming-3.jpg" alt="">

    </p>
</div>

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="https://simondanisch.github.io/ReferenceImages/gallery/axis_theming/media/axis_theming-4.jpg" alt="">

    </p>
</div>

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="https://simondanisch.github.io/ReferenceImages/gallery/axis_theming/media/axis_theming-5.jpg" alt="">

    </p>
</div>

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="https://simondanisch.github.io/ReferenceImages/gallery/axis_theming/media/axis_theming-6.jpg" alt="">

    </p>
</div>

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="https://simondanisch.github.io/ReferenceImages/gallery/axis_theming/media/axis_theming-7.jpg" alt="">

    </p>
</div>

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="https://simondanisch.github.io/ReferenceImages/gallery/axis_theming/media/axis_theming-8.jpg" alt="">

    </p>
</div>

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="https://simondanisch.github.io/ReferenceImages/gallery/axis_theming/media/axis_theming-9.jpg" alt="">

    </p>
</div>

```
