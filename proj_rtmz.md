---
---
**RTMZ** (previously RTMX) is a tech demo that I developed in the mid 90s.

The goal for the demo was that of showing off the real-time 3D rendering capabilities that I accumulated in years of personal R&D, as a teenager with a passion for computer graphics and games. Thankfully, this landed my first job in the game industry. Nothing sells like a cool demo.

In 2022 I [released](https://github.com/dpasca/rtmz) the old source code on GitHub for historical purposes.

The demo is written mostly in 'C' (C++ still had major performance issues at the time), and it ran on MS-DOS with VGA and SVGA resolutions on a 256 colors palette.

Major features are:

- Gouraud shading
- Texture mapping
- Basic lighting and material properties
- Z-Buffer (optional)
- Cool menu interface

#### My work on the project

- I wrote a rasterizer wih subpixel accuracy
- Implemented a materials system, within the limitations of 256 colors
- Wrote readers for *OBJ*, *3D Studio* and *Videoscape 3D* formats
- Implemented a cool 3D UI and record+playback system for demo purposes

#### What I learned

- This was the testbed for my early 3D rendering
- Portions of my 3D library mimicked OpenGL calls, which at the time was not available on PC


