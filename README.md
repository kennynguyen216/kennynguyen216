<div align="center">

# Kennedy Nguyen

**Graphics &middot; Engines &middot; Systems &middot; Applied AI** &nbsp;|&nbsp; Computer Science @ LSU, Class of 2027

I build real-time systems from the metal up: Vulkan engines, global illumination, and most recently a ray-traced game running on a GPU my team built in 24 hours.

[Portfolio](https://kennynguyen216.github.io/portfolio/) &nbsp;&middot;&nbsp; [LinkedIn](https://www.linkedin.com/in/kennedynguyen216) &nbsp;&middot;&nbsp; [Email](mailto:kennedyn216@gmail.com)

*Open to 2027 new-grad roles in graphics, engines, GPU and systems software.*

</div>

## 2026 at a glance

**Placed at 4 of 4 hackathons this year:**

| Event | Result | Project |
|---|---|---|
| **HackUTD 2026** | 1st Place, NVIDIA Track | [KennyCraft](#kennycraft) |
| **GeauxHack 2026** | 1st Place, Advanced (Top) Bracket | [FirstPrinciples](#firstprinciples) |
| **KnightHacks IX** | 1st BNY, 1st Neon, 3rd AMD ($6K+) | [GEarth](#gearth) |
| **WiCS Hackathon 2026** | 2nd Place, Advanced Bracket & Best Presentation | [3 Minutes to Rage](#more-projects) |

## Featured work

### [KennyCraft](https://github.com/Sweet-Rice/kennycraft-alpha)

**Ray-traced Minecraft on a custom FPGA GPU, built by three people in 24 hours.** 1st Place, NVIDIA Track at HackUTD 2026.

My teammate built the TPU, an 8-lane SIMD RISC-V processor with a hardware ray unit, on an Arty A7. I wrote everything that runs on it.

- **Engine on a 32 KB budget:** Q16 fixed-point math (no FPU, no divider), voxel DDA ray tracing bit-exact with the hardware ray unit, chunk streaming from DDR3, mobs and a Nether, all with no malloc and 40 bytes of data memory to spare.
- **0.73 &rarr; 405 fps** at 160&times;120 (cycle-accurate sim at 100 MHz; display-bound 60 fps on the board) through hardware&ndash;software co-design: a spill-free, branch-free SIMD kernel, ray setup overlapped with async hardware traversal, and core changes that cut a cycle from every instruction.
- **Every optimization pixel-identical** to a plain C reference renderer, checked with golden-image tests.
- **Nemotron agents in an on-chain economy:** villagers, a banker, a trader and builders using tool calls, with KennyCoin escrow settled on Solana devnet and dollars from Capital One's Nessie API.

`C` `RISC-V` `SystemVerilog` `Verilator` `Vivado` `NVIDIA Nemotron` `Solana` `Python`

### [FirstPrinciples](https://github.com/kennynguyen216/FirstPrinciples)

**A cross-platform C++20 game engine and game, built in 42 hours.** 1st Place, Advanced (Top) Bracket at GeauxHack 2026.

- **Engine:** Windows and macOS via Vulkan/Metal (SDL3 GPU), a Qt scene editor, ECS, hot-reloadable C++ scripts, P2P multiplayer and GPU meshlet culling: about 46K lines with tests and benchmarks.
- **Memory and concurrency core** (written by hand): reserve/commit virtual-memory arenas, page-backed pool allocators, and a fiber job system with assembly context switching and guard-paged stacks.
- **Ray-traced Schwarzschild black holes** with a photon ring, lensed accretion disk and gravitational redshift, driving the game's gravity-slingshot physics.
- **Audio:** ray-cast occlusion with acoustic materials, room reverb, Doppler, and proximity voice chat (48 kHz Opus over encrypted UDP).

`C++20` `SDL3 GPU` `Vulkan` `Metal` `GLSL` `Qt` `Jolt` `Opus`

### [Mirabilis & Nox](https://github.com/kennynguyen216/Mirabilis)

| Before the shadow pass | After the shadow pass |
|:---:|:---:|
| [![Sponza before the Mirabilis shadow pass](https://raw.githubusercontent.com/kennynguyen216/Mirabilis/main/docs/media/mirabilis-before-shadows.png)](https://github.com/kennynguyen216/Mirabilis/blob/main/docs/media/mirabilis-before-shadows.mp4) | [![Sponza after the Mirabilis shadow pass](https://raw.githubusercontent.com/kennynguyen216/Mirabilis/main/docs/media/mirabilis-after-shadows.png)](https://github.com/kennynguyen216/Mirabilis/blob/main/docs/media/mirabilis-after-shadows.mp4) |

<p align="center"><sub>Click either frame to watch the walkthrough.</sub></p>

**My C++20/Vulkan engine, with Nox, a hybrid real-time global illumination renderer.**

- **Nox GI:** screen-space tracing, distance fields and a surface cache at a **7.19 ms** median frame time on an RTX 3060 Laptop GPU. Trimmed **~490 MiB** of GPU memory and compacted shadow acceleration structures from **278 to 130 MiB**.
- **Engine:** glTF scenes with PBR, HDR, shadows and post-processing, an ImGui editor, EnTT ECS, Jolt physics, and .NET 10 C# scripts with live reload during Play.
- **Movement:** fixed 120 Hz Source-style controls with stencil-masked, momentum-preserving portals.

`C++20` `Vulkan` `GLSL` `EnTT` `Jolt` `C# / .NET 10` `SDL2` `ImGui`

**[Watch the shadow pass](https://github.com/kennynguyen216/Mirabilis/blob/main/docs/media/mirabilis-after-shadows.mp4)** &nbsp;&middot;&nbsp; **[Watch the movement run](https://github.com/kennynguyen216/Mirabilis/blob/main/docs/media/mirabilis-movement-time-trial.mp4)**

### [GEarth](https://github.com/liangricky7/GEarth)

**An AI society simulation of 1,100 LLM agents on a 3D globe.** 1st BNY, 1st Neon and 3rd AMD at KnightHacks IX ([Devpost](https://devpost.com/software/diarockets)).

- Served Qwen3 with vLLM across two NVIDIA DGX Sparks and an AMD GPU at up to 96% GPU utilization.
- Wrote the C++20/Vulkan replay viewer: PBR, shadow maps, HDR and bloom, procedural oceans and grass, and a globe with trade routes and events. A 17 MB simulation year compresses to a ~270 KB replay.

`C++20` `Vulkan` `GLSL` `Python` `vLLM` `Qwen3` `Neon PostgreSQL`

### [SigmaNova](https://github.com/kennynguyen216/SigmaNova)

<p align="center">
  <a href="https://github.com/kennynguyen216/SigmaNova">
    <img src="./assets/captures/sigmanova-remnant-demo.gif" width="480" alt="SigmaNova procedural supernova collapsing into a colorful nebular remnant">
  </a>
</p>

A real-time volumetric supernova: a procedural red supergiant collapses, flashes and expands into a cooling nebula. Ray marching sped up from **24.0 ms to 6.84 ms** through profiling.

`C++` `OpenGL` `GLSL` `GPU Profiling`

## More projects

| Project | What it is | Built with |
|---|---|---|
| **[3 Minutes to Rage](https://github.com/liangricky7/tspmo3-3MinutesToRage)** | Microphone-driven party game; 2nd Place and Best Presentation at WiCS 2026. | Unity, C# |
| **[Alfred](https://github.com/kennynguyen216/Alfred-AI-Student-Assistant)** | Local-first multi-agent student assistant with document, email and calendar tools. | C#, ASP.NET Core, SQLite, Ollama |
| **[Jarvis](https://github.com/kennynguyen216/Jarvis)** | Voice-controlled vision assistant driving a camera, scene analysis and spoken replies. | Python, OpenCV, Gemini, Arduino |

## Experience

- **Software Engineer Intern, LSU CARTS** (Jun. 2026 &ndash; present): shipped a production C# agent that lets Louisiana DOTD engineers query statewide crash data in plain English, using RAG text-to-SQL with self-hosted LLMs; cut latency 44%.
- **Undergraduate AI/ML Researcher, LSU ATHENA Lab** (Sep. 2026 &ndash; present): 98.0% macro F1 fine-tuning a vision transformer on an NVIDIA DGX Spark; caught train/test leakage in the dataset.

## Toolbox

**Graphics and engines:** C++20, Vulkan, OpenGL, SDL3 GPU, GLSL, ray tracing, global illumination, ECS, Jolt<br>
**Systems and hardware:** C, RISC-V, SystemVerilog, SIMD, fixed-point, FPGA (Vivado, Verilator), job systems, custom allocators<br>
**AI and backend:** C#, Python, ASP.NET Core, PyTorch, vLLM, NVIDIA Nemotron, RAG, Qdrant, SQLite<br>
**Tools:** Git, CMake, Premake, Docker, Perforce, OpenTelemetry, Google Cloud

---

<div align="center">

More at **[my portfolio](https://kennynguyen216.github.io/portfolio/)** &nbsp;&middot;&nbsp; Let's talk on **[LinkedIn](https://www.linkedin.com/in/kennedynguyen216)**

</div>
