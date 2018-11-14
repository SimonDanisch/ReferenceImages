## Orthographic Camera

```julia
using Makie
 using GeometryTypes

 x = Vec3f0(0); baselen = 0.2f0; dirlen = 1f0
 # create an array of differently colored boxes in the direction of the 3 axes
 rectangles = [
     (FRect3D(Vec3f0(x), Vec3f0(dirlen, baselen, baselen)), RGBAf0(1,0,0,1)),
     (FRect3D(Vec3f0(x), Vec3f0(baselen, dirlen, baselen)), RGBAf0(0,1,0,1)),
     (FRect3D(Vec3f0(x), Vec3f0(baselen, baselen, dirlen)), RGBAf0(0,0,1,1))
 ]
 meshes = map(GLNormalMesh, rectangles)
 scene = mesh(merge(meshes))
 display(scene)
 cam = Makie.cameracontrols(scene)
 dir = scene.limits[].widths ./ 2.
 dir_scaled = Vec3f0(
     dir[1] * scene.transformation.scale[][1],
     0.0,
     dir[3] * scene.transformation.scale[][2],
 )
 cam.upvector[] = (0.0, 0.0, 1.0)
 cam.lookat[] = scene.limits[].origin + dir_scaled
 cam.eyeposition[] = (cam.lookat[][1], cam.lookat[][2] + 6.3, cam.lookat[][3])
 cam.projectiontype[] = AbstractPlotting.Orthographic
 update_cam!(scene, cam)
 # stop scene display from centering, which would overwrite the camera paramter we just set
 scene.center = false
 scene


```
```@raw html

<div style="display:inline-block"><p style="display:inline-block; text-align: center">1<br><img src="/home/sd/ReferenceImages/recordings/orthographic_camera/media/image.jpg" alt="1<br>">
</p></div>
```
