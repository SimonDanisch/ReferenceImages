## Line with varying colors

```@raw html
<pre class='hljl'>
<span class='hljl-k'>using</span><span class='hljl-t'> </span><span class='hljl-n'>Makie</span><span class='hljl-t'>
 </span><span class='hljl-k'>using</span><span class='hljl-t'> </span><span class='hljl-n'>ColorSchemes</span><span class='hljl-t'>      </span><span class='hljl-cs'># colormaps galore</span><span class='hljl-t'>


 </span><span class='hljl-n'>t</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>range</span><span class='hljl-p'>(</span><span class='hljl-ni'>0</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>stop</span><span class='hljl-oB'>=</span><span class='hljl-ni'>1</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>length</span><span class='hljl-oB'>=</span><span class='hljl-ni'>500</span><span class='hljl-p'>)</span><span class='hljl-t'> </span><span class='hljl-cs'># time steps</span><span class='hljl-t'>

 </span><span class='hljl-n'>θ</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-p'>(</span><span class='hljl-ni'>6</span><span class='hljl-n'>π</span><span class='hljl-p'>)</span><span class='hljl-t'> </span><span class='hljl-oB'>.*</span><span class='hljl-t'> </span><span class='hljl-n'>t</span><span class='hljl-t'>    </span><span class='hljl-cs'># angles</span><span class='hljl-t'>

 </span><span class='hljl-n'>x</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>t</span><span class='hljl-t'> </span><span class='hljl-oB'>.*</span><span class='hljl-t'> </span><span class='hljl-n'>cos</span><span class='hljl-oB'>.</span><span class='hljl-p'>(</span><span class='hljl-n'>θ</span><span class='hljl-p'>)</span><span class='hljl-t'> </span><span class='hljl-cs'># x coords of spiral</span><span class='hljl-t'>
 </span><span class='hljl-n'>y</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>t</span><span class='hljl-t'> </span><span class='hljl-oB'>.*</span><span class='hljl-t'> </span><span class='hljl-n'>sin</span><span class='hljl-oB'>.</span><span class='hljl-p'>(</span><span class='hljl-n'>θ</span><span class='hljl-p'>)</span><span class='hljl-t'> </span><span class='hljl-cs'># y coords of spiral</span><span class='hljl-t'>

 </span><span class='hljl-n'>p1</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>lines</span><span class='hljl-p'>(</span><span class='hljl-t'>
     </span><span class='hljl-n'>x</span><span class='hljl-p'>,</span><span class='hljl-t'>
     </span><span class='hljl-n'>y</span><span class='hljl-p'>,</span><span class='hljl-t'>
     </span><span class='hljl-n'>color</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>t</span><span class='hljl-p'>,</span><span class='hljl-t'>
     </span><span class='hljl-n'>colormap</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>ColorSchemes</span><span class='hljl-oB'>.</span><span class='hljl-n'>magma</span><span class='hljl-oB'>.</span><span class='hljl-n'>colors</span><span class='hljl-p'>,</span><span class='hljl-t'>
     </span><span class='hljl-n'>linewidth</span><span class='hljl-oB'>=</span><span class='hljl-ni'>8</span><span class='hljl-p'>)</span><span class='hljl-t'>

 </span><span class='hljl-n'>cm</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>colorlegend</span><span class='hljl-p'>(</span><span class='hljl-t'>
     </span><span class='hljl-n'>p1</span><span class='hljl-p'>[</span><span class='hljl-k'>end</span><span class='hljl-p'>],</span><span class='hljl-t'>             </span><span class='hljl-cs'># access the plot of Scene p1</span><span class='hljl-t'>
     </span><span class='hljl-n'>raw</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-kc'>true</span><span class='hljl-p'>,</span><span class='hljl-t'>          </span><span class='hljl-cs'># without axes or grid</span><span class='hljl-t'>
     </span><span class='hljl-n'>camera</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>campixel!</span><span class='hljl-p'>,</span><span class='hljl-t'>  </span><span class='hljl-cs'># gives a concrete bounding box in pixels</span><span class='hljl-t'>
                          </span><span class='hljl-cs'># so that the `vbox` gives you the right size</span><span class='hljl-t'>
     </span><span class='hljl-n'>width</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-p'>(</span><span class='hljl-t'>            </span><span class='hljl-cs'># make the colorlegend longer so it looks nicer</span><span class='hljl-t'>
         </span><span class='hljl-ni'>30</span><span class='hljl-p'>,</span><span class='hljl-t'>              </span><span class='hljl-cs'># the width</span><span class='hljl-t'>
         </span><span class='hljl-ni'>540</span><span class='hljl-t'>              </span><span class='hljl-cs'># the height</span><span class='hljl-t'>
     </span><span class='hljl-p'>)</span><span class='hljl-t'>
     </span><span class='hljl-p'>)</span><span class='hljl-t'>

 </span><span class='hljl-n'>scene_final</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>vbox</span><span class='hljl-p'>(</span><span class='hljl-n'>p1</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>cm</span><span class='hljl-p'>)</span><span class='hljl-t'> </span><span class='hljl-cs'># put the colorlegend and the plot together in a `vbox`</span><span class='hljl-t'>


</span>
</pre>

```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="http://simondanisch.github.io/ReferenceImages/gallery/line_with_varying_colors/media/image.jpg" alt="">

    </p>
</div>

```
