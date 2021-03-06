## Explicit frame rendering

```@raw html
<pre class='hljl'>
<span class='hljl-k'>using</span><span class='hljl-t'> </span><span class='hljl-n'>Makie</span><span class='hljl-t'>
 </span><span class='hljl-k'>using</span><span class='hljl-t'> </span><span class='hljl-n'>ModernGL</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>GLMakie</span><span class='hljl-t'>
 </span><span class='hljl-k'>using</span><span class='hljl-t'> </span><span class='hljl-n'>GLFW</span><span class='hljl-t'>

 </span><span class='hljl-n'>GLMakie</span><span class='hljl-oB'>.</span><span class='hljl-n'>opengl_renderloop</span><span class='hljl-p'>[]</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-p'>(</span><span class='hljl-n'>screen</span><span class='hljl-p'>)</span><span class='hljl-t'> </span><span class='hljl-oB'>-&gt;</span><span class='hljl-t'> </span><span class='hljl-n'>nothing</span><span class='hljl-t'>
 </span><span class='hljl-k'>function</span><span class='hljl-t'> </span><span class='hljl-nf'>update_loop</span><span class='hljl-p'>(</span><span class='hljl-n'>m</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>buff</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>screen</span><span class='hljl-p'>)</span><span class='hljl-t'>
     </span><span class='hljl-k'>for</span><span class='hljl-t'> </span><span class='hljl-n'>i</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-ni'>1</span><span class='hljl-oB'>:</span><span class='hljl-ni'>20</span><span class='hljl-t'>
         </span><span class='hljl-n'>GLFW</span><span class='hljl-oB'>.</span><span class='hljl-nf'>PollEvents</span><span class='hljl-p'>()</span><span class='hljl-t'>
         </span><span class='hljl-n'>buff</span><span class='hljl-t'> </span><span class='hljl-oB'>.=</span><span class='hljl-t'> </span><span class='hljl-n'>rand</span><span class='hljl-oB'>.</span><span class='hljl-p'>(</span><span class='hljl-n'>Point3f0</span><span class='hljl-p'>)</span><span class='hljl-t'> </span><span class='hljl-oB'>.*</span><span class='hljl-t'> </span><span class='hljl-nfB'>20f0</span><span class='hljl-t'>
         </span><span class='hljl-n'>m</span><span class='hljl-p'>[</span><span class='hljl-ni'>1</span><span class='hljl-p'>]</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>buff</span><span class='hljl-t'>
         </span><span class='hljl-n'>GLMakie</span><span class='hljl-oB'>.</span><span class='hljl-nf'>render_frame</span><span class='hljl-p'>(</span><span class='hljl-n'>screen</span><span class='hljl-p'>)</span><span class='hljl-t'>
         </span><span class='hljl-n'>GLFW</span><span class='hljl-oB'>.</span><span class='hljl-nf'>SwapBuffers</span><span class='hljl-p'>(</span><span class='hljl-n'>GLMakie</span><span class='hljl-oB'>.</span><span class='hljl-nf'>to_native</span><span class='hljl-p'>(</span><span class='hljl-n'>screen</span><span class='hljl-p'>))</span><span class='hljl-t'>
         </span><span class='hljl-nf'>glFinish</span><span class='hljl-p'>()</span><span class='hljl-t'>
     </span><span class='hljl-k'>end</span><span class='hljl-t'>
 </span><span class='hljl-k'>end</span><span class='hljl-t'>
 </span><span class='hljl-n'>scene</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>meshscatter</span><span class='hljl-p'>(</span><span class='hljl-nf'>rand</span><span class='hljl-p'>(</span><span class='hljl-n'>Point3f0</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>10</span><span class='hljl-oB'>^</span><span class='hljl-ni'>4</span><span class='hljl-p'>)</span><span class='hljl-t'> </span><span class='hljl-oB'>.*</span><span class='hljl-t'> </span><span class='hljl-nfB'>20f0</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-n'>screen</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>AbstractPlotting</span><span class='hljl-oB'>.</span><span class='hljl-nf'>backend_display</span><span class='hljl-p'>(</span><span class='hljl-n'>GLMakie</span><span class='hljl-oB'>.</span><span class='hljl-nf'>GLBackend</span><span class='hljl-p'>(),</span><span class='hljl-t'> </span><span class='hljl-n'>scene</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-n'>meshplot</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>scene</span><span class='hljl-p'>[</span><span class='hljl-k'>end</span><span class='hljl-p'>]</span><span class='hljl-t'>
 </span><span class='hljl-n'>buff</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-nf'>rand</span><span class='hljl-p'>(</span><span class='hljl-n'>Point3f0</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-ni'>10</span><span class='hljl-oB'>^</span><span class='hljl-ni'>4</span><span class='hljl-p'>)</span><span class='hljl-t'> </span><span class='hljl-oB'>.*</span><span class='hljl-t'> </span><span class='hljl-nfB'>20f0</span><span class='hljl-p'>;</span><span class='hljl-t'>
 </span><span class='hljl-nf'>update_loop</span><span class='hljl-p'>(</span><span class='hljl-n'>meshplot</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>buff</span><span class='hljl-p'>,</span><span class='hljl-t'> </span><span class='hljl-n'>screen</span><span class='hljl-p'>)</span><span class='hljl-t'>
 </span><span class='hljl-n'>GLMakie</span><span class='hljl-oB'>.</span><span class='hljl-n'>opengl_renderloop</span><span class='hljl-p'>[]</span><span class='hljl-t'> </span><span class='hljl-oB'>=</span><span class='hljl-t'> </span><span class='hljl-n'>GLMakie</span><span class='hljl-oB'>.</span><span class='hljl-n'>renderloop</span><span class='hljl-t'> </span><span class='hljl-cs'># restore previous loop</span><span class='hljl-t'>
 </span><span class='hljl-n'>scene</span><span class='hljl-t'>

</span>
</pre>

```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="http://simondanisch.github.io/ReferenceImages/gallery/explicit_frame_rendering/media/image.jpg" alt="">

    </p>
</div>

```
