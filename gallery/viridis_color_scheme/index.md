## Viridis color scheme

```@raw html
<pre class='hljl'>
<span class='hljl-k'>using</span><span class='hljl-t'> </span><span class='hljl-n'>Makie</span><span class='hljl-t'>

 </span><span class='hljl-n'>c</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>to_colormap</span><span class='hljl-p'>(</span><span class='hljl-sc'>:viridis</span><span class='hljl-p'>)</span><span class='hljl-t'> </span><span class='hljl-cs'># get colors of colormap</span><span class='hljl-t'>

 </span><span class='hljl-nf'>image</span><span class='hljl-p'>(</span><span class='hljl-t'>         </span><span class='hljl-cs'># to plot colors, an image is best</span><span class='hljl-t'>
    </span><span class='hljl-nfB'>0..10</span><span class='hljl-p'>,</span><span class='hljl-t'>      </span><span class='hljl-cs'># x range</span><span class='hljl-t'>
    </span><span class='hljl-nfB'>0..1</span><span class='hljl-p'>,</span><span class='hljl-t'>       </span><span class='hljl-cs'># y range</span><span class='hljl-t'>
    </span><span class='hljl-nf'>hcat</span><span class='hljl-p'>(</span><span class='hljl-n'>c</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>c</span><span class='hljl-p'>),</span><span class='hljl-t'> </span><span class='hljl-cs'># reshape this to a matrix for the colors</span><span class='hljl-t'>
    </span><span class='hljl-n'>show_axis</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-kc'>false</span><span class='hljl-t'> </span><span class='hljl-cs'># don&#39;t show axes</span><span class='hljl-t'>
 </span><span class='hljl-p'>)</span><span class='hljl-t'>


</span>
</pre>

```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="http://juliaplots.org/MakieReferenceImages/gallery//viridis_color_scheme/media/image.jpg" alt="">

    </p>
</div>

```
