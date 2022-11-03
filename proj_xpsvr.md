An experimental flight simulator built to mimic the F-35
Lighting jet fighter. The project targeted VR for full-immersion.

Avionics display includes the famous 2-screen touch display of the F-35
and its windowing system that allows to configure the panels and to
maximize and minimize various elements.

Rendering is performed with the OYK Game's rendering engine which I
originally wrote for mobile games, and that I later expanded for PC GPUs
and OpenGL 4.5.

See more details on the [XPSVR's blog](https://xpsvr.com/tag/flightsim).

![](https://xpsvr.com/wp-content/uploads/2018/04/sshot_180310_045322.jpg)

#### My work on the project

I was the sole developer on this project. The main tasks were:

- Writing the game engine responsible based on OpenGL and OpenAL
- Physically Based shaders, IBL and CSM (Cascaded Shadow Maps)
- Underlying rigid-body physics engine
- Flight model for the airplane and missiles
- Autopilot for the airplane and the weapons
- VR support for Oculus
- Custom image compression and geometry LOD for the terrain
- GUI system, customized to simulate the F-35 look and feel
- Advanced avionics such as TSD (Tactical Situation Display) with moving
cursor and DAS (Digital Aperture System), the see-throught system
- Floating HUD simulating Head Mounted Display

#### What I learned

- Building a simple FDM (Flight Dynamics Model)
- Weapon systems and guidance (Missile Launch Envelope, Proportional
Navigation, etc.)
- Building a basic autopilot to maintain orientation and altitude
- Building avionic displays
- The F-35 user interface
- Use of CSM for large terrains

