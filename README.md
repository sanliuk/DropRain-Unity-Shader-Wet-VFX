## What I've done:

So Basically I mad three different ways to make the same fx and I called the object  in the scene with the same name:
1 Cube ScrollShader
2 Cube AmplifyVFXGraph ( I added Amplify Shader on the project , if you face some issue I used last version of Amplify, and unity 2022.3.18f1)
3 Cube VFX Graph ShaderGraph

In the first one I creat the scrolling fx directly in the shader because is the first thing I thought when I watched the fx.
In the second one is used Amplyfy shader.
The second one is very similar to the 3rd because they use the vfx graph that makes particles and trails to creat the rain effect.
A camera capture instantly the fx and a Render Texture that I calle "RenderTex" records it in the texture.
So both of them (second and 3rd) use vfx graphs to make the effect because their shaders use the render texture.
![alt text](https://github.com/sanliuk/DropRain-Unity-Shader-Wet-VFX/blob/master/Screenshot%202024-04-11%20132714.png
)"My approach with camera and vfx graph method"
## Controllers:
# Speed,  wet/dry effect, tiling offset UV.

Speed of drops is controllable from the editor but you have to activate the "set speed" on the vfx graph and deactivate what I put (speed over lifetime). I preferred speed over lifetime because I thought it was more realistic.
Wet/dry fx is controllable from the editor with the 2 sliders: you can put smoothness and normal to 0 and this delete the fx.
Tiling & offset are all managable from editor.


## Final Considarations & Conclusion:

I made all this basically in one day. So , yes it can be improved.
The performance that requires this fx are not too high.

Drops fx is made with flipbooks textures to add realism to the effect.
A noise on shader or a more controlled turbolance on the  effects can make more random and realistic drops
Drops can be improved with a more glossy material, somethings that is shiny but with a bit of reflection too (but still depends on what we need..) 
Do we relly need something with metallic, albedo, normals, ecc.. for a small fx? This depends on the LOD we need for the game.


All materials and textures are mine.
I just used a some samples from unity hdrp project file so I have not included any package.
But I'm pretty sure that I have imported vfx graph package and enabled one option that gives more tools for vfx grap. But it should work even without and I'm sure you know it.
In case, if something is missing or for some issue let me know as soon as possible.

Thank you

If you want to watch the preview CLICK THIS IMAGE:

[![](https://github.com/sanliuk/DropRain-Unity-Shader-Wet-VFX/blob/master/Screenshot%202024-04-11%20165753.png)](https://youtu.be/5yO5I5KjFlI)
[![](https://github.com/sanliuk/DropRain-Unity-Shader-Wet-VFX/blob/master/Screenshot%202024-04-11%20165753.png)]([https://youtu.be/5yO5I5KjFlI](https://youtu.be/HmYk7PJzuuY))



# WARNING
If you have some issue with materials, pipelines, shaders, pink materials, please feel free to contact me

Instagram @sanliuk
:)


