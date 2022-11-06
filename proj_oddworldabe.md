In 1997 I worked on the PC port (Windows and MS-DOS) of the now famous [**Oddworld Abe's: Oddysee**](https://www.oddworld.com/oddworldgames/abes-oddysee/).

The game was originally written for the Sony PlayStation, which at the time had specialized hardware capabilities unavailable to consumer PCs, requiring creative solutions to achieve the same results with just a CPU. 
Although the game didn't use 3D graphics, it ran on a 640x240 resolution and 16-bit color. The PC version was required to run at 640x480 with the same color resolution, with no hardware acceleration, using CPUs of the caliber of a *Pentium 120*.

My approach was to continue to use a 640x240 base resolution, but upscaling it with a cheap but effective smoothing filter that was fast enough for the target CPUs.

I also wrote an [MDEC](https://psx-spx.consoledev.net/macroblockdecodermdec/) (Macroblock Decoder) simulator, to playback the movie assets in the original PlayStation format. The clips were essential to the narration of the game and were sometimes mixed with the live animation.

Video decoding had specialized hardware on the PSX, but had to be done with the CPU on PC, requiring some special optimizations to maintain the necessary frame rate to decode the 320x240 video clips and upscale them to 640x480.

#### My work on the project

- Wrote a rasterizer capable of rendering the PlayStation graphics primitives with a CPU on PC
- MDEC simulation capable of playing native MJPEG PlayStation videos on PC
- Various tasks to adapt and port the original code

#### What I learned

- In-depth PlayStation's GPU calls
- Optimization techniques for 16-bit color rendering on SVGA resolution
- MDEC CODEC definition and implementation

