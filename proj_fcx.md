---
---
An arcade flight combat game with more than 1M downloads.

[Fractal Combat X](https://oykgames.com/fractal-combat-x/) (successor of [Fractal Combat](https://oykgames.com/fractal-combat/)), is an
arcade flight combat game for mobile phones that has reached a wide
distribution across multiple markets around the world.

It's built with and in-house game engine which I developed in C++ on top of
OpenGL ES. The game featues a continuous terrain LOD capable of showing
high detail at a very far distance with no percepible far clipping.

See the join technical presentation with Intel at GDC 2015, ["Getting There First: OpenGL ES 3.1 and Intel Extensions in Fractal Combat X"](https://vdocuments.net/getting-there-first-open-gles31fractalcombatx.html)

#### My work on the project

I was the sole developer on this project except for the Android platform. The main tasks were:

- Writing the underlying game engine
- Terrain LOD system with run-time light baking
- Implementation of OpenGL ES 3.1 tesselation, when available
- Dynamic skyline, with stratosphere and sun glare effects
- Dynamic destruction model for any 3D object
- Shadow mapping and IBL suitable for mobile
- VR support for Oculus GearVR, Google Cardboard or similar
- Custom image texture and audio compression
- Fractal terrain generation for certain stages
- 3D audio based on OpenAL
- GUI system, HUD

#### What I learned

- Terrain LOD and light baking on low-spec mobile systems
- OpenGL ES optimization for various mobile targets
- Use of in-app purchase and advertisement API calls
- Implementation of fun game controls for arcade flight combat games
- VR techniqes for playability and to improve comfort for the player

