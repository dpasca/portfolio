---
---
An image viewer capable of building composites of a stack of images with transparent regions. Source code at [github.com/gugenstudio/xComp](https://github.com/gugenstudio/xComp)

This tool was built to visualize region updates of a render on top of previous renders, in real-time. Images found in a chosen folder to scan for, are quickly composited with alpha blending in a stack. OpenColorIO transformations are optionally added to the composite image, which can be saved out as a PNG.

#### My work on the project

I was the sole developer on this project. The main tasks were:

- Setting up an multi-platform UI infrastructure with Dear ImGui and GLFW
- Implementation and use of OpenEXR and OpenColorIO
- Image compositing with alpha blending and resampling
- UI to manage EXR layers and masks

#### What I learned

- Build and usage of OpenEXR and OpenColorIO

