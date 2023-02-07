## Undergraduate Dissertation 2021: Comparing Lighting Methods Using GPU Hardware Accelerated Ray Tracing

**About this project:** For my third year final project, I explored the implementations of ray traced reflections, shadows, global illumination and ambient occlusion shaders and compared their performance and visual profiles. The shaders created for this project are written in the Slang shader language and make use of the DirectX12 API for ray tracing. These are launched from Falcor, a piece of software used for internal research at NVidia.

The final dissertation reached a word count of 12600 and achieved a first class grade of 77%.

### Abstract

When implementing ray traced lighting effects it is important to understand how the scenes in which these effects are deployed will affect their visual impact and performance metrics. This paper explores implementation of ray traced reflections, shadows, global illumination and ambient occlusion shaders in order to determine ideal optimisations and combinations of effects in different archetypical graphical scenes. The strengths and weaknesses of each effect is evaluated based on their performance measured against other ray traced effects and rasterised equivalents, as well as their subjective visual improvements. The results of this project determine an ideal combination of ray traced graphical effects in different scene types, including outdoor urban environments, outdoor rural environments and indoor environments.

### 1. Ray traced reflections shader
<iframe width="1280" height="725" src="https://www.youtube.com/embed/lVp3G2o0_ug" title="Páraic Bradley Ray Traced Reflections Shader" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

This video shows the naive ray traced reflections shader in an urban environment and demonstrates how changing the roughness cutoff will impact the final image.

### 2. Ray traced shadows shader
<iframe width="1280" height="725" src="https://www.youtube.com/embed/fC4gOE64zE0" title="Páraic Bradley Ray Traced Shadows Shader" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

This video demonstrates two possible approaches to ray traced shadows. The first approach considers every light source for every pixel on screen, and the second approach considers only a single light source per frame for every pixel. The second approach improves performance, but results in a noisy output image, so requires a robust denoising solution or for data to be accumulated over multiple frames.

### 3. Ray traced global illumination

<iframe width="1280" height="725" src="https://www.youtube.com/embed/Iu9ajc-PVJY" title="Páraic Bradley Ray Traced Global Illumination Shader" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

This video shows a simple ray traced global illumination shader which calculates only a single bounce of indirect light. This produces a noisy output, so requires data to be accumulated over multiple frames. Although being recorded at a high bitrate, sections of the video showcasing the raw noisy output suffer from extreme compression when uploaded to YouTube and this is unavoidable.

This shader can also be combined with the previous ray traced shadows shader to provide a more complete lighting model and a more attractive final image.

### 4. Ray traced ambient occlusion

<iframe width="1280" height="725" src="https://www.youtube.com/embed/lqITkLesNZU" title="Páraic Bradley Ray Traced Ambient Occlusion Shader" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

This video showcases ray traced ambient occlusion and demonstrates both the noisy, raw output and the clean final image when data is accumulated over multiple frames. As with the global illumination shader, sections of the video showing the noisy output are unfortunately greatly harmed by YouTube compression.
