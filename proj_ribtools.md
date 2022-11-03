[RibTools](https://github.com/dpasca/RibTools) is an experimental open-source implementation of the basic Pixar's RenderMan REYES rendering architecture. The parser is able to parse simple RenderMan rib scene and shaders which run on a custom VM.
Rendering of the micropolygons is performed via SIMD CPU instructions.

Parallelism is implemented at all levels:
- Instruction level (adaptive N-way SIMD)
- Many-core hardware (multi-threading)
- Network-distributed rendering (custom protocol over TCP/IP)

![](https://github.com/dpasca/RibTools/raw/master/docs/progress/2010-01-26_killeroo_properly_displaced.png)

See more details on: [Implementing an experimental RenderMan compliant REYES renderer]({{ site.baseurl }}/images/2010_04_Implementing_REYES_RibTools_up_20221110.pdf)

#### My work on the project

I was the sole developer on this project except. The main tasks were:

- Writing the rib scene parser
- RenderMan shader parser and compiler
- Implementation of a custom shader VM with SIMD opcodes
- Implementation of a REYES-style micropolygon renderer
- Flexible SIMD functions to write N-way parallel code
- Display and debugging infrastrcture in in OpenGL
- Server-client code for distributed rendering

#### What I learned

- REYES-style micropolygon rendering
- Writing a shader compiler and VM
- Writing N-way vector and thread parallelism
- Basics of implementation of network-distributed rendering

