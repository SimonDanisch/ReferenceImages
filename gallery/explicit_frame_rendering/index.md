## Explicit frame rendering

```julia
using Makie
 using ModernGL, Makie, GLMakie
 using GLFW

 GLMakie.opengl_renderloop[] = (screen) -> nothing
 function update_loop(m, buff, screen)
     for i = 1:20
         GLFW.PollEvents()
         buff .= rand.(Point3f0) .* 20f0
         m[1] = buff
         GLMakie.render_frame(screen)
         GLFW.SwapBuffers(GLMakie.to_native(screen))
         glFinish()
     end
 end
 scene = meshscatter(rand(Point3f0, 10^4) .* 20f0)
 display(scene)
 meshplot = scene[end]
 buff = rand(Point3f0, 10^4) .* 20f0;
 screen = GLMakie.global_gl_screen();
 @time update_loop(meshplot, buff, screen)
 GLMakie.opengl_renderloop[] = GLMakie.renderloop # restore previous loop
 # when done:
 GLMakie.destroy!(screen)
 scene


```
```@raw html

<div style="display:inline-block">
    <p style="display:inline-block; text-align: center">
        <img src="https://raw.githubusercontent.com/SimonDanisch/ReferenceImages/master/gallery/explicit_frame_rendering/media/image.jpg" alt="">

    </p>
</div>

```
