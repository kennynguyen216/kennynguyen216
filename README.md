<div align="center">

# Kennedy Nguyen

**Computer Science @ LSU &middot; Graphics &middot; Simulation &middot; AI Systems &middot; Interactive Technology**

I build real-time systems you can see, feel, and interact with.

[Portfolio](https://kennynguyen216.github.io/portfolio/) &nbsp;&middot;&nbsp; [LinkedIn](https://www.linkedin.com/in/kennedynguyen216) &nbsp;&middot;&nbsp; [Current Build](#currently-building) &nbsp;&middot;&nbsp; [Selected Work](#selected-work)

*Open to 2027 software engineering roles and internships.*

</div>

## Currently Building

### [Mirabilis](https://github.com/kennynguyen216/Mirabilis)

| Before the shadow pass | After the shadow pass |
|:---:|:---:|
| [![Sponza before the Mirabilis shadow pass](https://raw.githubusercontent.com/kennynguyen216/Mirabilis/main/docs/media/mirabilis-before-shadows.png)](https://github.com/kennynguyen216/Mirabilis/blob/main/docs/media/mirabilis-before-shadows.mp4) | [![Sponza after the Mirabilis shadow pass](https://raw.githubusercontent.com/kennynguyen216/Mirabilis/main/docs/media/mirabilis-after-shadows.png)](https://github.com/kennynguyen216/Mirabilis/blob/main/docs/media/mirabilis-after-shadows.mp4) |

<p align="center"><sub>Click either frame to watch the corresponding walkthrough.</sub></p>

Mirabilis is my C++20/Vulkan engine prototype, bringing together editor-authored scenes, Source/Quake-style movement, momentum-preserving player portals, Jolt physics, and C# gameplay scripting.

- Implements GPU mesh/material pipelines, textured glTF/GLB scene loading, real-time shadows, ambient occlusion, and screen-space global illumination.
- Provides an ImGui scene editor with hierarchical transforms, inspector/gizmos, editable colliders, and JSON persistence.
- Integrates EnTT scene entities and Jolt rigid bodies with editor authoring, fixed-step simulation, interpolation, and Play/reset snapshots.
- Hosts .NET 10 gameplay scripts with inspector-editable fields and live code reload: save C# during Play and keep the current scene, physics state, and supported script fields.
- Combines fixed-**120 Hz** Source/Quake-style movement, timed courses, stencil-mask portal rendering, wall-opening collision, and momentum-preserving traversal.

`C++20` `Vulkan` `GLSL` `EnTT` `Jolt Physics` `C# / .NET 10` `SDL2` `ImGui` `CMake`

**[Explore the repository](https://github.com/kennynguyen216/Mirabilis)** &nbsp;&middot;&nbsp; **[Watch the shadow pass](https://github.com/kennynguyen216/Mirabilis/blob/main/docs/media/mirabilis-after-shadows.mp4)** &nbsp;&middot;&nbsp; **[Watch the movement run](https://github.com/kennynguyen216/Mirabilis/blob/main/docs/media/mirabilis-movement-time-trial.mp4)** &nbsp;&middot;&nbsp; **[View my portfolio](https://kennynguyen216.github.io/portfolio/)**

## Selected Work

### [GEarth](https://github.com/liangricky7/GEarth)

**[Three prize wins at Knight Hacks IX](https://devpost.com/software/diarockets):**

- **BNY:** Financial Services Challenge
- **AMD:** Best Use of AMD Technologies
- **Neon:** Best Use of Neon

A team-built AI society simulation connecting citizens, businesses, governments, trade, and diplomacy. A C# engine maintains the world while distributed Qwen3 inference drives agent decisions; a browser dashboard and native Vulkan viewer make the results explorable.

My contributions:

- Set up distributed Qwen3 inference across two NVIDIA DGX Spark systems and an AMD GPU.
- Developed the native C++20/Vulkan replay viewer, recording and launcher tooling, and meadow and market-square environments for inspecting the simulated world.

**Vulkan renderer highlights:**

- **Materials and lighting:** GLSL physically based shading with normal maps, metallic/roughness and emissive textures, sun shadow maps, and point/spot lighting.
- **Asset pipeline:** Static glTF/GLB scene loading, BC7-compressed DDS textures kept compressed on the GPU, mip selection, and camera/shadow visibility culling for imported environments such as Bistro.
- **HDR and post-processing:** Exposure control, bloom, sun glare, ACES-style tone mapping, sRGB output, and FXAA anti-aliasing.
- **Procedural environments:** Animated ocean waves and water reflections, plus GPU-generated rolling terrain, wind-bent grass, flowers, and moving cloud shadows. Distant wave detail is filtered to reduce visual aliasing.
- **Simulation playback:** A globe view with recorded country state, night lights, cargo routes, and event overlays. Packaged `.gearth` recordings support pause, seek, and looping without rerunning model inference; the viewer can also follow checkpoints from a running simulation through the API.

`C++20` `Vulkan` `GLSL` `C# / .NET` `Python` `Qwen3` `Distributed Inference` `Neon PostgreSQL`

**[Repository](https://github.com/liangricky7/GEarth)** &nbsp;&middot;&nbsp; **[Renderer details](https://github.com/liangricky7/GEarth/blob/main/renderer/GRAPHICS.md)** &nbsp;&middot;&nbsp; **[Devpost and awards](https://devpost.com/software/diarockets)**

### [SigmaNova](https://github.com/kennynguyen216/SigmaNova)

<p align="center">
  <a href="https://github.com/kennynguyen216/SigmaNova">
    <img src="./assets/captures/sigmanova-remnant-demo.gif" width="480" alt="SigmaNova procedural supernova collapsing into a colorful nebular remnant">
  </a>
</p>

A real-time C++/OpenGL visualization that stages a procedural red supergiant through collapse, flash, asymmetric ejecta expansion, and a cooling nebular remnant.

- Built a volumetric ray marcher with procedural FBM noise, emission and absorption, HDR bloom, tone mapping, and pulsar illumination.
- Cut initial frame time from about **24.0 ms to 6.84 ms** in the first shader optimization pass.
- Added non-blocking GPU timestamp queries, dynamic volume resolution, and pass-level performance reporting.

`C++` `OpenGL` `GLSL` `CMake` `GPU Profiling`

## More Projects

| Project | What I built | Core technologies |
|---|---|---|
| **[3 Minutes to Rage](https://github.com/liangricky7/tspmo3-3MinutesToRage)** | A fast-paced hackathon game with microphone-driven mechanics; contributed gameplay and player-feedback systems. | Unity, C# |
| **[Jarvis](https://github.com/kennynguyen216/Jarvis)** | A voice-controlled vision assistant that routes speech into camera movement, scene analysis, and spoken responses. | Python, OpenCV, Gemini, Arduino |
| **[Alfred](https://github.com/kennynguyen216/Alfred-AI-Student-Assistant)** | A local-first multi-agent student assistant with document, email, and calendar tools backed by a local model. | C#, ASP.NET Core, SQLite, Ollama |

## About Me

- B.S. Computer Science candidate at Louisiana State University, Class of 2027.
- Research Software Engineer at LSU CARTS, building AI-assisted crash analytics tools.
- Interested in graphics and rendering, simulation, applied AI, computer vision, and human-computer interaction.
- Most at home turning ambitious ideas into working prototypes, then profiling, documenting, and refining them.

## Technical Toolbox

**Graphics and simulation:** C++, Vulkan, OpenGL, GLSL, Jolt Physics, EnTT, CMake<br>
**AI and backend:** C#, Python, ASP.NET Core, agent workflows, RAG, Ollama<br>
**Interactive systems:** SDL2, Unity, Arduino, OpenCV, PySerial<br>
**Data and tools:** SQL, SQLite, Git, JavaScript

---

See more at **[my portfolio](https://kennynguyen216.github.io/portfolio/)** or reach me through **[LinkedIn](https://www.linkedin.com/in/kennedynguyen216)**.
