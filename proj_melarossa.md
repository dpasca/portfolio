### 3D display for Melarossa health app (2022)

A wasm package for the 3D display of a human figure (male and female) with morphing animation of vertices between different body weights and fat distributions. See the [announcement](https://www.melarossa.it/dieta/simulatore-3d/) (in Italian).

![](https://www.melarossa.it/wp-content/uploads/2022/06/somatotipo-3d.jpg?x75677)

#### My work on the project

- Adapted my current C++ and OpenGL ES-based 3D engine for the job
- Added necessary system code and build scripts to compile and run via Emscripten
- Wrote a shader for deformation and blending to morph individual body sections at different BMIs
- Implemented Image Based Lighting (IBL) for added realism
- Implemented real-time shadow mapping, also working on mobile phones

#### What I learned

- Deployment and optimization of WebGL 1.0 and 2.0 via Emscripten

