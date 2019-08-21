## StatsMakie

```@raw html
<pre class='hljl'>
<span class='hljl-k'>using</span><span class='hljl-t'> </span><span class='hljl-n'>Makie</span><span class='hljl-t'>
 </span><span class='hljl-k'>using</span><span class='hljl-t'> </span><span class='hljl-n'>StatsMakie</span><span class='hljl-t'>
 </span><span class='hljl-k'>using</span><span class='hljl-t'> </span><span class='hljl-n'>DataFrames</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>RDatasets</span><span class='hljl-t'>
 </span><span class='hljl-k'>using</span><span class='hljl-t'> </span><span class='hljl-n'>StatsMakie</span><span class='hljl-oB'>:</span><span class='hljl-t'> </span><span class='hljl-n'>linear</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>smooth</span><span class='hljl-t'>

 </span><span class='hljl-n'>N</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-ni'>1000</span><span class='hljl-t'>
 </span><span class='hljl-n'>a</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>rand</span><span class='hljl-p'>(</span><span class='hljl-ni'>1</span><span class='hljl-oB'>:</span><span class='hljl-ni'>2</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>N</span><span class='hljl-p'>)</span><span class='hljl-t'> </span><span class='hljl-cs'># a discrete variable</span><span class='hljl-t'>
 </span><span class='hljl-n'>b</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>rand</span><span class='hljl-p'>(</span><span class='hljl-ni'>1</span><span class='hljl-oB'>:</span><span class='hljl-ni'>2</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>N</span><span class='hljl-p'>)</span><span class='hljl-t'> </span><span class='hljl-cs'># a discrete variable</span><span class='hljl-t'>
 </span><span class='hljl-n'>x</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>randn</span><span class='hljl-p'>(</span><span class='hljl-n'>N</span><span class='hljl-p'>)</span><span class='hljl-t'> </span><span class='hljl-cs'># a continuous variable</span><span class='hljl-t'>
 </span><span class='hljl-n'>y</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> @</span><span class='hljl-oB'>.</span><span class='hljl-t'> </span><span class='hljl-n'>x</span><span class='hljl-t'> </span><span class='hljl-oB'>*</span><span class='hljl-t'> </span><span class='hljl-n'>a</span><span class='hljl-t'> </span><span class='hljl-oB'>+</span><span class='hljl-t'> </span><span class='hljl-nfB'>0.8</span><span class='hljl-oB'>*</span><span class='hljl-nf'>randn</span><span class='hljl-p'>()</span><span class='hljl-t'> </span><span class='hljl-cs'># a continuous variable</span><span class='hljl-t'>
 </span><span class='hljl-n'>z</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>x</span><span class='hljl-t'> </span><span class='hljl-oB'>.+</span><span class='hljl-t'> </span><span class='hljl-n'>y</span><span class='hljl-t'> </span><span class='hljl-cs'># a continuous variable</span><span class='hljl-t'>
 </span><span class='hljl-nd'>@substep</span><span class='hljl-t'>

 </span><span class='hljl-nf'>scatter</span><span class='hljl-p'>(</span><span class='hljl-n'>x</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>y</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>markersize</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nfB'>0.2</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-nd'>@substep</span><span class='hljl-t'>

 </span><span class='hljl-nf'>scatter</span><span class='hljl-p'>(</span><span class='hljl-nf'>Group</span><span class='hljl-p'>(</span><span class='hljl-n'>a</span><span class='hljl-p'>),</span><span class='hljl-t'> </span><span class='hljl-n'>x</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>y</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>markersize</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nfB'>0.2</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-nd'>@substep</span><span class='hljl-t'>

 </span><span class='hljl-nf'>scatter</span><span class='hljl-p'>(</span><span class='hljl-nf'>Group</span><span class='hljl-p'>(</span><span class='hljl-n'>a</span><span class='hljl-p'>),</span><span class='hljl-t'> </span><span class='hljl-n'>x</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>y</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>color</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-p'>[</span><span class='hljl-sc'>:black</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-sc'>:red</span><span class='hljl-p'>],</span><span class='hljl-t'> </span><span class='hljl-n'>markersize</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nfB'>0.2</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-nd'>@substep</span><span class='hljl-t'>

 </span><span class='hljl-nf'>scatter</span><span class='hljl-p'>(</span><span class='hljl-nf'>Group</span><span class='hljl-p'>(</span><span class='hljl-n'>marker</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>a</span><span class='hljl-p'>),</span><span class='hljl-t'> </span><span class='hljl-n'>x</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>y</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>markersize</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nfB'>0.2</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-nd'>@substep</span><span class='hljl-t'>

 </span><span class='hljl-nf'>scatter</span><span class='hljl-p'>(</span><span class='hljl-nf'>Group</span><span class='hljl-p'>(</span><span class='hljl-n'>marker</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>a</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>color</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>b</span><span class='hljl-p'>),</span><span class='hljl-t'> </span><span class='hljl-n'>x</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>y</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>markersize</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nfB'>0.2</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-nd'>@substep</span><span class='hljl-t'>

 </span><span class='hljl-nf'>scatter</span><span class='hljl-p'>(</span><span class='hljl-nf'>Group</span><span class='hljl-p'>(</span><span class='hljl-n'>marker</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>a</span><span class='hljl-p'>),</span><span class='hljl-t'> </span><span class='hljl-nf'>Style</span><span class='hljl-p'>(</span><span class='hljl-n'>color</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>z</span><span class='hljl-p'>),</span><span class='hljl-t'> </span><span class='hljl-n'>x</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>y</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-nd'>@substep</span><span class='hljl-t'>

 </span><span class='hljl-nf'>scatter</span><span class='hljl-p'>(</span><span class='hljl-nf'>Group</span><span class='hljl-p'>(</span><span class='hljl-n'>color</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>a</span><span class='hljl-p'>),</span><span class='hljl-t'> </span><span class='hljl-n'>x</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>y</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-nf'>Style</span><span class='hljl-p'>(</span><span class='hljl-n'>markersize</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>z</span><span class='hljl-t'> </span><span class='hljl-oB'>./</span><span class='hljl-t'> </span><span class='hljl-ni'>10</span><span class='hljl-p'>))</span><span class='hljl-t'>
 </span><span class='hljl-nd'>@substep</span><span class='hljl-t'>

 </span><span class='hljl-nf'>plot</span><span class='hljl-p'>(</span><span class='hljl-n'>linear</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>x</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>y</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-nd'>@substep</span><span class='hljl-t'>

 </span><span class='hljl-nf'>plot</span><span class='hljl-p'>(</span><span class='hljl-n'>linear</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-nf'>Group</span><span class='hljl-p'>(</span><span class='hljl-n'>a</span><span class='hljl-p'>),</span><span class='hljl-t'> </span><span class='hljl-n'>x</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>y</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-nd'>@substep</span><span class='hljl-t'>

 </span><span class='hljl-nf'>scatter</span><span class='hljl-p'>(</span><span class='hljl-nf'>Group</span><span class='hljl-p'>(</span><span class='hljl-n'>a</span><span class='hljl-p'>),</span><span class='hljl-t'> </span><span class='hljl-n'>x</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>y</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>markersize</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nfB'>0.2</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-nf'>plot!</span><span class='hljl-p'>(</span><span class='hljl-n'>linear</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-nf'>Group</span><span class='hljl-p'>(</span><span class='hljl-n'>a</span><span class='hljl-p'>),</span><span class='hljl-t'> </span><span class='hljl-n'>x</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>y</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-nd'>@substep</span><span class='hljl-t'>

 </span><span class='hljl-nf'>plot</span><span class='hljl-p'>(</span><span class='hljl-n'>linear</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-nf'>Group</span><span class='hljl-p'>(</span><span class='hljl-n'>linestyle</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>a</span><span class='hljl-p'>),</span><span class='hljl-t'> </span><span class='hljl-n'>x</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>y</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-nd'>@substep</span><span class='hljl-t'>

 </span><span class='hljl-n'>N</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-ni'>200</span><span class='hljl-t'>
 </span><span class='hljl-n'>x</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-ni'>10</span><span class='hljl-t'> </span><span class='hljl-oB'>.*</span><span class='hljl-t'> </span><span class='hljl-nf'>rand</span><span class='hljl-p'>(</span><span class='hljl-n'>N</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-n'>a</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>rand</span><span class='hljl-p'>(</span><span class='hljl-ni'>1</span><span class='hljl-oB'>:</span><span class='hljl-ni'>2</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>N</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-n'>y</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>sin</span><span class='hljl-oB'>.</span><span class='hljl-p'>(</span><span class='hljl-n'>x</span><span class='hljl-p'>)</span><span class='hljl-t'> </span><span class='hljl-oB'>.+</span><span class='hljl-t'> </span><span class='hljl-nfB'>0.5</span><span class='hljl-t'> </span><span class='hljl-oB'>.*</span><span class='hljl-t'> </span><span class='hljl-nf'>rand</span><span class='hljl-p'>(</span><span class='hljl-n'>N</span><span class='hljl-p'>)</span><span class='hljl-t'> </span><span class='hljl-oB'>.+</span><span class='hljl-t'> </span><span class='hljl-n'>cos</span><span class='hljl-oB'>.</span><span class='hljl-p'>(</span><span class='hljl-n'>x</span><span class='hljl-p'>)</span><span class='hljl-t'> </span><span class='hljl-oB'>.*</span><span class='hljl-t'> </span><span class='hljl-n'>a</span><span class='hljl-t'>
 </span><span class='hljl-nd'>@substep</span><span class='hljl-t'>

 </span><span class='hljl-nf'>scatter</span><span class='hljl-p'>(</span><span class='hljl-nf'>Group</span><span class='hljl-p'>(</span><span class='hljl-n'>a</span><span class='hljl-p'>),</span><span class='hljl-t'> </span><span class='hljl-n'>x</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>y</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-nf'>plot!</span><span class='hljl-p'>(</span><span class='hljl-n'>smooth</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-nf'>Group</span><span class='hljl-p'>(</span><span class='hljl-n'>a</span><span class='hljl-p'>),</span><span class='hljl-t'> </span><span class='hljl-n'>x</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>y</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-nd'>@substep</span><span class='hljl-t'>

 </span><span class='hljl-nf'>plot</span><span class='hljl-p'>(</span><span class='hljl-n'>histogram</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>y</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-nd'>@substep</span><span class='hljl-t'>

 </span><span class='hljl-nf'>plot</span><span class='hljl-p'>(</span><span class='hljl-n'>histogram</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>x</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>y</span><span class='hljl-p'>)</span><span class='hljl-t'>

 </span><span class='hljl-nd'>@substep</span><span class='hljl-t'>

 </span><span class='hljl-nf'>plot</span><span class='hljl-p'>(</span><span class='hljl-nf'>histogram</span><span class='hljl-p'>(</span><span class='hljl-n'>nbins</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-ni'>30</span><span class='hljl-p'>),</span><span class='hljl-t'> </span><span class='hljl-n'>x</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>y</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-nd'>@substep</span><span class='hljl-t'>

 </span><span class='hljl-nf'>wireframe</span><span class='hljl-p'>(</span><span class='hljl-nf'>histogram</span><span class='hljl-p'>(</span><span class='hljl-n'>nbins</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-ni'>30</span><span class='hljl-p'>),</span><span class='hljl-t'> </span><span class='hljl-n'>x</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>y</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-nd'>@substep</span><span class='hljl-t'>

 </span><span class='hljl-n'>iris</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>RDatasets</span><span class='hljl-oB'>.</span><span class='hljl-nf'>dataset</span><span class='hljl-p'>(</span><span class='hljl-s'>&quot;datasets&quot;</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-s'>&quot;iris&quot;</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-nf'>scatter</span><span class='hljl-p'>(</span><span class='hljl-nf'>Data</span><span class='hljl-p'>(</span><span class='hljl-n'>iris</span><span class='hljl-p'>),</span><span class='hljl-t'> </span><span class='hljl-nf'>Group</span><span class='hljl-p'>(</span><span class='hljl-sc'>:Species</span><span class='hljl-p'>),</span><span class='hljl-t'> </span><span class='hljl-sc'>:SepalLength</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-sc'>:SepalWidth</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-nd'>@substep</span><span class='hljl-t'>
 </span><span class='hljl-cs'># use Position.stack to signal that you want bars stacked vertically rather than superimposed</span><span class='hljl-t'>
 </span><span class='hljl-nf'>plot</span><span class='hljl-p'>(</span><span class='hljl-n'>Position</span><span class='hljl-oB'>.</span><span class='hljl-n'>stack</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>histogram</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-nf'>Data</span><span class='hljl-p'>(</span><span class='hljl-n'>iris</span><span class='hljl-p'>),</span><span class='hljl-t'> </span><span class='hljl-nf'>Group</span><span class='hljl-p'>(</span><span class='hljl-sc'>:Species</span><span class='hljl-p'>),</span><span class='hljl-t'> </span><span class='hljl-sc'>:SepalLength</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-nd'>@substep</span><span class='hljl-t'>

 </span><span class='hljl-nf'>wireframe</span><span class='hljl-p'>(</span><span class='hljl-t'>
     </span><span class='hljl-nf'>density</span><span class='hljl-p'>(</span><span class='hljl-n'>trim</span><span class='hljl-oB'>=</span><span class='hljl-kc'>true</span><span class='hljl-p'>),</span><span class='hljl-t'>
     </span><span class='hljl-nf'>Data</span><span class='hljl-p'>(</span><span class='hljl-n'>iris</span><span class='hljl-p'>),</span><span class='hljl-t'> </span><span class='hljl-nf'>Group</span><span class='hljl-p'>(</span><span class='hljl-sc'>:Species</span><span class='hljl-p'>),</span><span class='hljl-t'> </span><span class='hljl-sc'>:SepalLength</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-sc'>:SepalWidth</span><span class='hljl-p'>,</span><span class='hljl-t'>
     </span><span class='hljl-n'>transparency</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-kc'>true</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>linewidth</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nfB'>0.1</span><span class='hljl-t'>
 </span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-nd'>@substep</span><span class='hljl-t'>

 </span><span class='hljl-nf'>scatter</span><span class='hljl-p'>(</span><span class='hljl-t'>
     </span><span class='hljl-nf'>Data</span><span class='hljl-p'>(</span><span class='hljl-n'>iris</span><span class='hljl-p'>),</span><span class='hljl-t'>
     </span><span class='hljl-nf'>Group</span><span class='hljl-p'>(</span><span class='hljl-n'>marker</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-sc'>:Species</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>color</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>bycolumn</span><span class='hljl-p'>),</span><span class='hljl-t'>
     </span><span class='hljl-sc'>:SepalLength</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-p'>(</span><span class='hljl-sc'>:PetalLength</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-sc'>:PetalWidth</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-nd'>@substep</span><span class='hljl-t'>

 </span><span class='hljl-nf'>barplot</span><span class='hljl-p'>([</span><span class='hljl-s'>&quot;hi&quot;</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-s'>&quot;ima&quot;</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-s'>&quot;string&quot;</span><span class='hljl-p'>],</span><span class='hljl-t'> </span><span class='hljl-nf'>rand</span><span class='hljl-p'>(</span><span class='hljl-ni'>3</span><span class='hljl-p'>))</span><span class='hljl-t'>
 </span><span class='hljl-nd'>@substep</span><span class='hljl-t'>


</span>
</pre>

```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="http://juliaplots.org/MakieReferenceImages/gallery//statsmakie/media/image10.jpg" alt="">

    </p>
</div>

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="http://juliaplots.org/MakieReferenceImages/gallery//statsmakie/media/image11.jpg" alt="">

    </p>
</div>

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="http://juliaplots.org/MakieReferenceImages/gallery//statsmakie/media/image12.jpg" alt="">

    </p>
</div>

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="http://juliaplots.org/MakieReferenceImages/gallery//statsmakie/media/image14.jpg" alt="">

    </p>
</div>

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="http://juliaplots.org/MakieReferenceImages/gallery//statsmakie/media/image15.jpg" alt="">

    </p>
</div>

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="http://juliaplots.org/MakieReferenceImages/gallery//statsmakie/media/image16.jpg" alt="">

    </p>
</div>

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="http://juliaplots.org/MakieReferenceImages/gallery//statsmakie/media/image17.jpg" alt="">

    </p>
</div>

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="http://juliaplots.org/MakieReferenceImages/gallery//statsmakie/media/image18.jpg" alt="">

    </p>
</div>

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="http://juliaplots.org/MakieReferenceImages/gallery//statsmakie/media/image19.jpg" alt="">

    </p>
</div>

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="http://juliaplots.org/MakieReferenceImages/gallery//statsmakie/media/image2.jpg" alt="">

    </p>
</div>

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="http://juliaplots.org/MakieReferenceImages/gallery//statsmakie/media/image20.jpg" alt="">

    </p>
</div>

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="http://juliaplots.org/MakieReferenceImages/gallery//statsmakie/media/image21.jpg" alt="">

    </p>
</div>

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="http://juliaplots.org/MakieReferenceImages/gallery//statsmakie/media/image22.jpg" alt="">

    </p>
</div>

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="http://juliaplots.org/MakieReferenceImages/gallery//statsmakie/media/image23.jpg" alt="">

    </p>
</div>

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="http://juliaplots.org/MakieReferenceImages/gallery//statsmakie/media/image3.jpg" alt="">

    </p>
</div>

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="http://juliaplots.org/MakieReferenceImages/gallery//statsmakie/media/image4.jpg" alt="">

    </p>
</div>

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="http://juliaplots.org/MakieReferenceImages/gallery//statsmakie/media/image5.jpg" alt="">

    </p>
</div>

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="http://juliaplots.org/MakieReferenceImages/gallery//statsmakie/media/image6.jpg" alt="">

    </p>
</div>

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="http://juliaplots.org/MakieReferenceImages/gallery//statsmakie/media/image7.jpg" alt="">

    </p>
</div>

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="http://juliaplots.org/MakieReferenceImages/gallery//statsmakie/media/image8.jpg" alt="">

    </p>
</div>

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="http://juliaplots.org/MakieReferenceImages/gallery//statsmakie/media/image9.jpg" alt="">

    </p>
</div>

```
