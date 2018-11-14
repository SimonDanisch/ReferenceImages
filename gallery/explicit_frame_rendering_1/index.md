## Explicit frame rendering

```julia
using Makie
 using ModernGL, Makie
 using GLFW

 Makie.GLMakie.opengl_renderloop[] = (screen) -> nothing
 function update_loop(m, buff, screen)
     for i = 1:20
         GLFW.PollEvents()
         buff .= rand.(Point3f0) .* 20f0
         m[1] = buff
         Makie.GLMakie.render_frame(screen)
         GLFW.SwapBuffers(Makie.GLMakie.to_native(screen))
         glFinish()
     end
 end
 scene = meshscatter(rand(Point3f0, 10^4) .* 20f0)
 display(scene)
 meshplot = scene[end]
 buff = rand(Point3f0, 10^4) .* 20f0;
 screen = Makie.GLMakie.global_gl_screen();
 @time update_loop(meshplot, buff, screen)
 Makie.GLMakie.opengl_renderloop[] = Makie.GLMakie.renderloop # restore previous loop
 # when done:
 Makie.GLMakie.destroy!(screen)
 scene


```
```@raw html

<div style="display:inline-block"><p style="display:inline-block; text-align: center">1<br><img src="/home/sd/ReferenceImages/recordings/explicit_frame_rendering_1/media/image.jpg" alt="1<br>">
</p></div>
```
