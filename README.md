## At first glance..
Upon receiving the task, my initial thought was to leverage a standard shader graph, rather than focusing on a particle effect. 
However, the mention of the VFX graph sparked curiosity: why was it suggested? With some research and reflection, it became clear. 
The intention was to craft an effect that mimics raindrops glistening and reflecting light as they slide down surfaces, achieved through the clever use of scrolling textures via render textures. 
This realization was enlightening.

Consequently, I pivoted from my original approach, which involved a scrolling shader designed to simulate rain splash and dripping effects. 
I embarked on developing a new dripping effect on a flat surface, utilizing particles emitted within the VFX Graph. These particles were captured by a camera, creating a continuously moving texture.

I preserved both the initial and new versions of the effect and further explored an alternative using the Amplify Shader, in place of the Shader Graph. 
My objective now is to ensure that all versions not only appear convincing and credible but also allow for customization in tiling and rain intensity.

Finally, I will consider ways to optimize memory usage, making the effect more efficient.

## What I've done:

So Basically I mad three different ways to make the same fx and I called the object  in the scene with the same name:
1 Cube ScrollShader
2 Cube AmplifyVFXGraph ( I added Amplify Shader on the project , if you face some issue I used last vrsion of Amplify, and unity 2022.3.18f1. Or we can watch it together on my screen)
3 Cube VFX Graph ShaderGraph

In the first one I creat the scrolling fx directly in the shader because is the first thing I thought when I watched the fx.
In the second one is used Amplyfy shader.
The second one is very similar to the 3rd because they use the vfx graph that makes particles and trails to creat the rain effect.
A camera capture instantly the fx and a Render Texture that I calle "RenderTex" records it in the texture.
So both of them (second and 3rd) use vfx graphs to make the effect because their shaders use the render texture.
![alt text](https://github.com/sanliuk/RainDrop/blob/master/Screenshot%202024-04-11%20132714.png
)"My approach with camera and vfx graph method"
## Controllers:
# Speed,  wet/dry effect, tiling offset UV.

Speed of drops is controllable from the editor but you have to activate the "set speed" on the vfx graph and deactivate what I put (speed over lifetime). I preferred speed over lifetime because I thought it was more realistic.
Wet/dry fx is controllable from the editor with the 2 sliders: you can put smoothness and normal to 0 and this delete the fx.
Tiling & offset are all managable from editor.


## Final Considarations & Conclusion:

I made all this basically in one day. So , yes it can be improved.
As I wrote in the mail to miss Hallikainen I can keep improving all of them or we can discuss togather in a call if you think is enough for you.
Now, the performance that requires this fx are not high at all but we can discuss together on which could be a nice solution and see what would be nice for the need we have.


Drops fx is made with flipbooks textures to add realism to the effect.
A noise on shader or a more controlled turbolance on the  effects can make more random and realistic drops
Drops can be improved with a more glossy material, somethings that is shiny but with a bit of reflection too (but still depends on what we need..) 
Do we relly need something with metallic, albedo, normals, ecc.. for a small fx? This depends on the LOD we need for the game.


All materials and textures are mine.
I just used a some samples from unity hdrp project file so I have not included any package.
But I'm pretty sure that I have imported vfx graph package and enabled one option that gives more tools for vfx grap. But it should work even without and I'm sure you know it.
In casa, if something is missing or some issue let me know as soon as possible.

I thank you all,
Best regards.

[![](https://github.com/sanliuk/RainDrop/blob/master/Screenshot%202024-04-11%20165753.png)](https://youtu.be/5yO5I5KjFlI)


Manuel
hosseini.manuel@gmail.com

