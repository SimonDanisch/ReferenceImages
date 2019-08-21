## Add and change points

```@raw html
<pre class='hljl'>
<span class='hljl-k'>using</span><span class='hljl-t'> </span><span class='hljl-n'>Makie</span><span class='hljl-t'>
 </span><span class='hljl-k'>using</span><span class='hljl-t'> </span><span class='hljl-n'>LinearAlgebra</span><span class='hljl-t'>

 </span><span class='hljl-n'>img</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>rand</span><span class='hljl-p'>(</span><span class='hljl-ni'>100</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>100</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-n'>scene</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>Scene</span><span class='hljl-p'>(</span><span class='hljl-n'>scale_plot</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-kc'>false</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>resolution</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-p'>(</span><span class='hljl-ni'>500</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>500</span><span class='hljl-p'>))</span><span class='hljl-t'>
 </span><span class='hljl-nf'>heatmap!</span><span class='hljl-p'>(</span><span class='hljl-n'>scene</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>img</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-n'>clicks</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>Node</span><span class='hljl-p'>(</span><span class='hljl-n'>Point2f0</span><span class='hljl-p'>[(</span><span class='hljl-ni'>0</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>0</span><span class='hljl-p'>)])</span><span class='hljl-t'>
 </span><span class='hljl-n'>blues</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>Node</span><span class='hljl-p'>(</span><span class='hljl-n'>Point2f0</span><span class='hljl-p'>[])</span><span class='hljl-t'>
 </span><span class='hljl-nf'>on</span><span class='hljl-p'>(</span><span class='hljl-n'>scene</span><span class='hljl-oB'>.</span><span class='hljl-n'>events</span><span class='hljl-oB'>.</span><span class='hljl-n'>mousebuttons</span><span class='hljl-p'>)</span><span class='hljl-t'> </span><span class='hljl-k'>do</span><span class='hljl-t'> </span><span class='hljl-n'>buttons</span><span class='hljl-t'>
     </span><span class='hljl-k'>if</span><span class='hljl-t'> </span><span class='hljl-nf'>ispressed</span><span class='hljl-p'>(</span><span class='hljl-n'>scene</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>Mouse</span><span class='hljl-oB'>.</span><span class='hljl-n'>left</span><span class='hljl-p'>)</span><span class='hljl-t'>
         </span><span class='hljl-n'>pos</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>to_world</span><span class='hljl-p'>(</span><span class='hljl-n'>scene</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-nf'>Point2f0</span><span class='hljl-p'>(</span><span class='hljl-n'>scene</span><span class='hljl-oB'>.</span><span class='hljl-n'>events</span><span class='hljl-oB'>.</span><span class='hljl-n'>mouseposition</span><span class='hljl-p'>[]))</span><span class='hljl-t'>
         </span><span class='hljl-n'>found</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-oB'>-</span><span class='hljl-ni'>1</span><span class='hljl-t'>
         </span><span class='hljl-n'>c</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>clicks</span><span class='hljl-p'>[]</span><span class='hljl-t'>
         </span><span class='hljl-k'>for</span><span class='hljl-t'> </span><span class='hljl-n'>i</span><span class='hljl-t'> </span><span class='hljl-kp'>in</span><span class='hljl-t'> </span><span class='hljl-ni'>1</span><span class='hljl-oB'>:</span><span class='hljl-nf'>length</span><span class='hljl-p'>(</span><span class='hljl-n'>c</span><span class='hljl-p'>)</span><span class='hljl-t'>
            </span><span class='hljl-k'>if</span><span class='hljl-t'> </span><span class='hljl-nf'>norm</span><span class='hljl-p'>(</span><span class='hljl-n'>pos</span><span class='hljl-t'> </span><span class='hljl-oB'>-</span><span class='hljl-t'> </span><span class='hljl-n'>c</span><span class='hljl-p'>[</span><span class='hljl-n'>i</span><span class='hljl-p'>])</span><span class='hljl-t'> </span><span class='hljl-oB'>&lt;</span><span class='hljl-t'> </span><span class='hljl-ni'>1</span><span class='hljl-t'>
                </span><span class='hljl-n'>found</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>i</span><span class='hljl-t'>
            </span><span class='hljl-k'>end</span><span class='hljl-t'>
         </span><span class='hljl-k'>end</span><span class='hljl-t'>
         </span><span class='hljl-k'>if</span><span class='hljl-t'> </span><span class='hljl-n'>found</span><span class='hljl-t'> </span><span class='hljl-oB'>&gt;=</span><span class='hljl-t'> </span><span class='hljl-ni'>1</span><span class='hljl-t'>
             </span><span class='hljl-n'>blues</span><span class='hljl-p'>[]</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>push!</span><span class='hljl-p'>(</span><span class='hljl-n'>blues</span><span class='hljl-p'>[],</span><span class='hljl-t'> </span><span class='hljl-n'>pos</span><span class='hljl-p'>)</span><span class='hljl-t'>
             </span><span class='hljl-nf'>deleteat!</span><span class='hljl-p'>(</span><span class='hljl-n'>clicks</span><span class='hljl-p'>[],</span><span class='hljl-t'> </span><span class='hljl-n'>found</span><span class='hljl-p'>)</span><span class='hljl-t'>
         </span><span class='hljl-k'>else</span><span class='hljl-t'>
             </span><span class='hljl-nf'>push!</span><span class='hljl-p'>(</span><span class='hljl-n'>clicks</span><span class='hljl-p'>[],</span><span class='hljl-t'> </span><span class='hljl-n'>pos</span><span class='hljl-p'>)</span><span class='hljl-t'>
         </span><span class='hljl-k'>end</span><span class='hljl-t'>
         </span><span class='hljl-n'>clicks</span><span class='hljl-p'>[]</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>clicks</span><span class='hljl-p'>[]</span><span class='hljl-t'>
    </span><span class='hljl-k'>end</span><span class='hljl-t'>
    </span><span class='hljl-k'>return</span><span class='hljl-t'>
 </span><span class='hljl-k'>end</span><span class='hljl-t'>
 </span><span class='hljl-n'>t</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>Theme</span><span class='hljl-p'>(</span><span class='hljl-n'>markersize</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-ni'>10</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>raw</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-kc'>true</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-nf'>scatter!</span><span class='hljl-p'>(</span><span class='hljl-n'>scene</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>t</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>clicks</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>color</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-sc'>:red</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>marker</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-sc'>&#39;+&#39;</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-n'>red_clicks</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>scene</span><span class='hljl-p'>[</span><span class='hljl-k'>end</span><span class='hljl-p'>]</span><span class='hljl-t'>
 </span><span class='hljl-nf'>scatter!</span><span class='hljl-p'>(</span><span class='hljl-n'>scene</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>t</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>blues</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>color</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-sc'>:blue</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>marker</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-sc'>&#39;o&#39;</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-nf'>center!</span><span class='hljl-p'>(</span><span class='hljl-n'>scene</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-nf'>RecordEvents</span><span class='hljl-p'>(</span><span class='hljl-n'>scene</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-s'>&quot;output&quot;</span><span class='hljl-p'>)</span><span class='hljl-t'>

</span>
</pre>

```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <video controls autoplay loop muted>
  <source src="http://juliaplots.org/MakieReferenceImages/gallery//add_and_change_points/media/video.mp4" type="video/mp4">
  Your browser does not support mp4. Please use a modern browser like Chrome or Firefox.
</video>

    </p>
</div>

```
