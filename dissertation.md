## Undergraduate Dissertation 2021: Comparing Lighting Methods Using GPU Hardware Accelerated Ray Tracing

**About this project:** For my third year final project, I explored the implementations of ray traced reflections, shadows, global illumination and ambient occlusion shaders and compared their performance and visual profiles. The shaders created for this project are written in the Slang shader language and make use of the DirectX12 API for ray tracing. These are launched from Falcor, a piece of software used for internal research at NVidia.

The final dissertation reached a word count of 12600 and achieved a first class grade of 77%.

### 1. [Ray traced reflections shader](https://www.youtube.com/watch?v=lVp3G2o0_ug)

![Bistro Exterior ray traced reflections](/images/reflections_bistroExterior.jpg)

![Sun Temple ray traced reflections](/images/reflections_SunTemple.jpg)

A naive ray traced reflections shader in an urban environment. 

The linked video shows the shader in motion and demonstrates how changing the roughness cutoff will impact the final image.

### 2. [Ray traced shadows shader](https://www.youtube.com/watch?v=fC4gOE64zE0)

![Arcade ray traced shadows](/images/shadows_Arcade.jpg)

Simple ray traced shadows.

The linked video demonstrates two possible approaches to ray traced shadows. The first approach considers every light source for every pixel on screen, and the second approach considers only a single light source per frame for every pixel. The second approach improves performance, but results in a noisy output image, so requires a robust denoising solution or for data to be accumulated over multiple frames.

### 3. [Ray traced global illumination](https://www.youtube.com/watch?v=Iu9ajc-PVJY)

![Bistro Exterior ray traced global illumination](/images/gi_BistroExterior.jpg)

![Emereald Square ray traced global illumination](/images/gi_EmeraldSquare.jpg)

Simple ray traced global illumination, with a single bounce of indirect light. Images show ray traced global illumination combined with ray traced shadows to provide a more complete and attractive final image.

The linked video shows the shader in motion. This shader produces a noisy output, so requires data to be accumulated over multiple frames. Although originally being recorded at a high bitrate, sections of the video showcasing the raw noisy output suffer unfortunately from extreme compression when uploaded to YouTube.

### 4. [Ray traced ambient occlusion](https://www.youtube.com/watch?v=lqITkLesNZU)

![Sun Temple ray traced ambient occlusiom](/images/ao_sunTemple.jpg)

![Sun Temple ray traced ambient occlusiom](/images/ao_bistroInterior.jpg)

The linked video showcases ray traced ambient occlusion and demonstrates both the noisy, raw output and the clean final image when data is accumulated over multiple frames. As with the global illumination shader, sections of the video showing the noisy output are unfortunately greatly harmed by YouTube compression.

### [Full Paper](/pdf/ParaicBradley_Dissertation_180165038.pdf)
