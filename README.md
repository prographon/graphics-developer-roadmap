# graphics-developer-roadmap

This repository contains different resources which may be helpful during your journey of becoming a graphics developer. The list is supported by [@prographon](https://github.com/prographon) community. Our current plans include finding more high-quality books, tutorials and articles, creating a step-by-step guide (roadmap) for becoming a graphics engineer and sharing knowledge about new edge-breaking technologies in Computer Graphics.

## How to start learning

### Required preparations

The first thing to note is that to become graphic/rendering developer you must really know a lot. Almost all engines are written in C++, so you must certainly learn it first before diving into rendering. Knowledge of computer architecture is also highly recommended, specifically GPU architecture. C++/other languages resources are **not** present in this roadmap, as they are not explicitly related to graphics. You can either learn these topics first and then return to graphics, or try learning everything in parallel - the choice is up to you.

### Starting point

One of the easiest way to touch graphics programming without dealing with real graphic APIs is to write a software rasterizer/raytracer. [Ssloy's tutorials](https://github.com/ssloy/tinyrenderer/wiki) contain two very well written tutorials: [tinyraytracer](https://github.com/ssloy/tinyraytracer/wiki) and [tinyrenderer](https://github.com/ssloy/tinyrenderer/wiki/Lesson-0:-getting-started). You can go through them first and get a good insight on how raytracing and graphic API implementation works, without even touching a real GPU.

### Parallel computing

The best way to get insight of how GPU work is to try to adapt your code for parallel processing. If you followed the first step, at this point you have a nice looking path tracer / renderer, which now you can speed up by porting your rendering code to [OpenCL]() or [Cuda](). These are the frameworks for general purpose GPU computing which are not yet graphic APIs, but introduce some new concepts with which you should become familiar. If you already tried to optimize your projects by utilizing multiple CPU cores, the process of porting should not be hard.

### OpenGL as first graphic API

 Now when you have a bit of understanding of how interact with GPU, you can finally dive into real graphic APIs. The opinions may vary, but the smoothest learning curve is achieved when you start from the simplest graphic APIs, such as OpenGL, and only after mastering it switching to more verbose, like DirectX 12 or Vulkan. Note that even with OpenGL you can write almost everything, including 2D renderer, first-person shooter game or general-purpose game engine. It is okay spending a year on a project which seemed simple at first glance, as long as it helps you to learn and give you a joy. For best start we suggest watching Cherno's [OpenGL series](https://www.youtube.com/watch?v=W3gAzLwfIP0&list=PLlrATfBNZ98foTJPJ_Ev03o2oq3-GGOS2&ab_channel=TheCherno) and going through [LearnOpenGL turorials](https://learnopengl.com/). Your main goal at this stage is to understand how GPU rendering works, implement classic algorithms like [shadow mapping](https://learnopengl.com/Advanced-Lighting/Shadows/Shadow-Mapping) and [deferred rendering](https://learnopengl.com/Advanced-Lighting/Deferred-Shading), and create your own [physically based renderer](https://academy.substance3d.com/courses/the-pbr-guide-part-1). We believe that these are the topics which any graphic engineer should understand to be ready for real job in rendering team.

### WIP

*This topic is not completed yet. If you want to speed up the process, feel free to contribute*



## Graphic API

### OpenGL

<img src="images/opengl-logo.png" height="150">

- [Learn OpenGL](https://learnopengl.com/) - modern (3.3+) OpenGL tutorial (phong lighting, shadow mapping, mesh loading, deferred rendering, PBR + IBL lighting) 
- [OpenGL step by step](http://ogldev.atspace.co.uk/) - modern (3.3+) OpenGL tutorial (phong lighting, shadow mapping, mesh loading, deferred rendering, skeletal animation)
- [OpenGL tutorial](http://www.opengl-tutorial.org/) - modern (3.3+) OpenGL tutorial (phong lighting, shadow mapping, text rendering, mesh loading)
- [OpenGL by The Cherno](https://www.youtube.com/watch?v=W3gAzLwfIP0&list=PLlrATfBNZ98foTJPJ_Ev03o2oq3-GGOS2&ab_channel=TheCherno) - step by step OpenGL course for beginners (basic 2D rendering, texturing, batching)

### Vulkan

<img src="images/vulkan-logo.png" height="150">

- [Vulkan 1.2 API Specifications](https://www.khronos.org/registry/vulkan/specs/1.2-extensions/html/index.html) - Official Vulkan specification by Khronos Group
- [Vulkan Tutorial](https://vulkan-tutorial.com/) - Vulkan tutorial teaching basics of the API (initializing context, drawing triangle, texturing, mesh loading)
- [API without Secrets: Introduction to Vulkan](https://software.intel.com/content/www/us/en/develop/articles/api-without-secrets-introduction-to-vulkan-preface.html) - in depth tutorial about Vulkan API (initializing context, swapchain, drawing triangle, descriptor sets) 
- [Vulkan Guide](https://github.com/KhronosGroup/Vulkan-Guide) - Vulkan guide by Khronos Group (graphic pipeline, layers, memory allocations, synchronization)
- [niagara: Building a Vulkan renderer from scratch](https://www.youtube.com/playlist?list=PL0JVLUVCkk-l7CWCn3-cdftR0oajugYvd) - In-depth lessons series about how to use few modern Vulkan rendering techniques, such as GPU culling & scene submission, cone culling, automatic occlusion culling, task/mesh shading, and others
- [Tips and Tricks: Vulkan Dos and Don’ts](https://developer.nvidia.com/blog/vulkan-dos-donts/) - Nvidia's tips for designing high performance Vulkan applications
- [Vulkanised](https://www.youtube.com/watch?v=1rDCNknSb2s&list=PLYO7XTAX41FPMg41svrVJA9stwcYCvdW0) - Open webinars about Vulkan best practices and pitfalls by Khronos Group
- [Writing an efficient Vulkan renderer](https://zeux.io/2020/02/27/writing-an-efficient-vulkan-renderer/) - Chapter about Vulkan renderer from GPU Zen 2 book in a form of the blogpost

### DirectX 12

<img src="images/directx12-logo.png" height="150">

- [Learning DirectX 12](https://www.3dgep.com/learning-directx-12-1/) - in depth tutorial about DirectX 12 API (graphic pipeline, command queues, descriptor sets, texturing)
- [Official DirectX 12 Graphics samples by Microsoft](https://github.com/microsoft/DirectX-Graphics-Samples)
- [Official DirectX documentation](https://docs.microsoft.com/en-us/windows/win32/directx)
- [Official DXIL documentation](https://github.com/microsoft/DirectXShaderCompiler/blob/master/docs/DXIL.rst)
- [DirectX supplementary specs (GitHub)](https://microsoft.github.io/DirectX-Specs/)
- [DirectX 3D Series](https://wiki.planetchili.net/index.php/Hardware_3D_Series_(C%2B%2B_DirectX_Graphics))
- [Braynzar soft DirectX 12 tutorials](https://www.braynzarsoft.net/viewtutorial/q16390-04-directx-12-braynzar-soft-tutorials)

## Books
- [Realtime Rendering](https://www.amazon.com/Real-Time-Rendering-Fourth-Tomas-Akenine-M%C3%B6ller/dp/1138627003) (graphics hardware, shading & lighting algorithms, ray tracing)
- [Physically Based Rendering: From Theory To Implementation](http://www.pbr-book.org/) (PBR, photorealistic rendering, sampling methods)
- [Substance PBR Guide](https://academy.substance3d.com/courses/the-pbr-guide-part-1)
- [Advanced Global Illumination](https://www.amazon.com/Advanced-Global-Illumination-Philip-Dutre/dp/1568813074) (global illumination algorithms, light transport theory, radiosity)
- [GPU Gems](https://developer.nvidia.com/gpugems/gpugems/contributors) (collections of different 3D graphics algorithms)
- [Ray Tracing in One Weekend Book Series](https://github.com/RayTracing/raytracing.github.io) (software ray tracing, BVH)
- [Collection of PDF books about graphics and programming](https://drive.google.com/drive/folders/1D-M15SvPxF1JqmzRt1UenQ1x6Zp_Ebb9?usp=sharing)
- [GPU Pro](https://www.amazon.com/GPU-Pro-Advanced-Rendering-Techniques/dp/1568814720) (like GPU Gems, but it's closer to state-of-art)

## Articles
- [Basic Theory of Physically-Based Rendering by Marmoset](https://marmoset.co/posts/basic-theory-of-physically-based-rendering/)
- [Physically Based Rendering in Filament](https://google.github.io/filament/Filament.html) - equations and theory behind the material and lighting models used in Filament.

## Tutorials
- [Ssloy's tutorials](https://github.com/ssloy/tinyrenderer/wiki) - tinyrenderer (software rasterizer), tinyraytacer (software ray-tracer)
- [Common techniques to improve shadow maps](https://docs.microsoft.com/en-us/windows/win32/dxtecharts/common-techniques-to-improve-shadow-depth-maps) - antialiasing algorithm for shadows, cascaded shadow maps, solutions to common problems (with DirectX 11 code snippets)
- [AMD RDNA2 Perfomance Guide](https://gpuopen.com/performance/)

## Courses
- [Advances in Real-Time Rendering in 3D Graphics and Games](http://advances.realtimerendering.com/)
- [GDC Vault](https://www.gdcvault.com/)
- [Interactive 3D Graphics (Eric Haines)](https://www.udacity.com/course/interactive-3d-graphics--cs291)

## Video courses
- [TU Wien Ray tracing course](https://www.youtube.com/playlist?list=PLujxSBD-JXgnGmsn7gEyN28P1DnRZG7qi) - A course on photorealistic rendering, ray tracing and global illumination at the TU Wien

## Digests
- [Two Minute Papers](https://www.youtube.com/channel/UCbfYPyITQ-7l4upoX8nvctg) - summaries of modern articles on computer graphics
- [Graphics Programming weekly](https://www.jendrikillner.com/tags/weekly/) - weekly newsletter with CG materials

## Blogs
- [Self Shadow](https://blog.selfshadow.com/) - Stephen Hill, principal rendering engineer, Lucasfilm Advanced Development Group
- [Wicked Engine Net](https://wickedengine.net/) - blog about computer graphics and game engine dev by graphics programmer at Sony
- [Ray Tracey's blog](http://raytracey.blogspot.com/) - Sam Lapere, scientific visualization devtech at Nvidia
- [Eric Heitz](https://eheitzresearch.wordpress.com/research/) - research scientist at Unity Technologies
- [Wenzel Jakob](http://rgl.epfl.ch/people/wjakob) - assistant professor leading the Realistic Graphics Lab at EPFL's School of Computer and Communication Sciences
- [Real-time rendering resources](https://www.realtimerendering.com/) - resources page for the book Real-Time Rendering and a lot of useful links
- [Alian Galvan](https://alain.xyz/blog) - graphics programmer at Marmoset about engine development, samples with different graphics API
- [Game Development by Sean](https://seanmiddleditch.com/) - game and engine development, common techniques
- [CODE517E](https://c0de517e.blogspot.com/) - blog about graphics by graphics programmer at Altera
- [Aras P](https://aras-p.info/blog/) - lead graphics programmer at Unity, contains many tricks and techniques
- [Arseny Kapoulkine](https://zeux.io/) - technical fellow at Roblox, Vulkan-related and mobile stuff
- [Adrian Courreges](http://www.adriancourreges.com/blog/) - collection of frame analysis during current decade of different games
- [Matt Pettineo](https://therealmjp.github.io/posts/) - lead graphics/engine programmer at Ready At Dawn Studios, articles about Spherical Gaussians and GPU Barriers
- [Emilio Lopez](http://www.elopezr.com/) - Senior Graphics Engineer at Playground Games. Previously making LEGO at Traveller's Tales.
- [Simon Coenen](https://simoncoenen.com/blog) - Platform Engineer at Studio Gobo, Brighton.
- [Jasper St. Pierre](https://blog.mecheye.net/) - Creator of [noclip.website](https://noclip.website/). Staff Graphics Software Engineer at Cryptic Studios. Also has a [YouTube channel](https://www.youtube.com/user/DaysAreRare).

## Useful sites
- [Shader Playground](http://shader-playground.timjones.io/) - powerful online shader compiler
- [Shadertoy](https://www.shadertoy.com/) - shader showcase sandbox
- [GPU info](https://gpuinfo.org/) - open database of Vulkan, GL and GLES devices, their capabilities and supported extensions
- [HexEd](https://hexed.it/) - browser-based hex editor

## Tools
- [RenderDoc](https://renderdoc.org/) - very powerful Vulkan, DirectX and OpenGL debugger with support of in-engine integration
- [AMD CodeXL](https://github.com/GPUOpen-Archive/CodeXL) - CPU/GPU debugger and profiler
- [AMD Compressonator](https://gpuopen.com/compressonator/) - tool for texture compression
- [AMD GPU Profiler](https://gpuopen.com/rgp/)
- [AMD Memory Visualizer](https://gpuopen.com/rmv/)
- [AMD Developer Panel](https://gpuopen.com/rdp/)
- [AMD GPU Analyzer](https://gpuopen.com/rga/) - offline compiling tool and ISA inspector
- [NVidia NSight](https://developer.nvidia.com/nsight-graphics) - powerful profiling tool, support of ray-tracing debugging
- [Intel GPA](https://software.intel.com/content/www/us/en/develop/tools/graphics-performance-analyzers.html)
- [Apple Metal debugger](https://developer.apple.com/documentation/metal/basic_tasks_and_concepts/viewing_your_gpu_workload_with_the_metal_debugger) - powerful macOS and iOS graphics debugger, profiler with shader debugging
- [ShaderED](https://shadered.org/) - shader IDE with lots of debugging utilities
- [Microsoft PIX](https://devblogs.microsoft.com/pix/introduction/) - powerful Windows and XBOX debugger and profiler
- [PowerVR SDK Tools](https://www.imaginationtech.com/developers/powervr-sdk-tools/) - collection of tools for graphics programming
- [Naga](https://github.com/gfx-rs/naga) - convert from one shader format into another
