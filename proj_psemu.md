In 1997 I started working on the [**PSEmu Pro**](https://handwiki.org/wiki/Software:PSEmu_Pro), the first PlayStation emulator.

**PSEmu Pro** was possibly also the most consequential of the PSX emulators, due
to its DLL plugin system that simplified the creation of more modern emulators, such as *ePSXe*.

Subsequent emulators could focus development on a subset of the hardware, while relying on existing plugins made for the *PSEmu Pro*, to support other key portions of the hardware such the GPU and the GTE.

My initial involvement was writing the [GPU](https://psx-spx.consoledev.net/graphicsprocessingunitgpu/) (Graphics Processing Unit) rendering emulation in software rendering.
I eventually joined the other two original developers (*Duddie* and *Tratax*), with the *Kazzuya* nickname, forming the final core team.

Once in the team, I worked on anything necessary, most notably the
[GTE](https://psx-spx.consoledev.net/geometrytransformationenginegte/) (Geometry Transformation Engine), and [MDEC](https://psx-spx.consoledev.net/macroblockdecodermdec/) (Macroblock Decoder) emulation.  Constantly balancing between performance and accuracy.

This was a non-commercial effort, done for the sake of the challenge
itself.
I worked on this in my spare time, coordinating the effort online via IRC (Internet Relay Chat).

#### My work on the project

- GPU software rendering emulation
- GTE emulation, used for 3D math
- MDEC emulation, used for video MJPEG-like decoding
- Gamepad controller plugin

#### What I learned

- Details about the PlayStation hardware
- Working with a fully-remote team
- Optimization techniques for fixed-point math operations
- Optimization techniques for video decoding

