A real-time demo that uses Spherical Harmonics (SH) to quickly apply Image Based Lighting (IBL) for diffuse and ambient lighting.

The user can paint on a virtual cube map to freely apply lighting without the limitation of classical light sources.

The SH coefficients for the IBL are calculated on the CPU at every frame. The rendering is performed in OpenGL with a shader that calculates lighting of each vertex based on those SH coefficients.

This technique is based on the famous paper: ["An Efficient Representation for Irradiance Environment Maps"](https://graphics.stanford.edu/papers/envmap/) by Ravi Ramamoorthi and Pat Hanrahan. I've since used Spherical Harmonics for diffused lighting or ambient lighting in every 3D engine that I wrote.

#### My work on the project

I was the sole developer on this project. The main tasks were:

- Implementation of the Spherical Harmonics coefficients on the CPU at every frame
- Shader that generates colors based on the SH coefficients
- A basic UI with an on-screen console and painting of the cube maps
- A system to record and replay events, for the demo mode

#### What I learned

- Application of Spherical Harmonics for lighting
