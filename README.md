# Davide Pasca's programmer portfolio

I consider programming computers the ultimate form of exploration and creativity, everything else is secondary. I'm an R&D guy at the core, although I also appreciate publishing products, because it's something that can have a direct impact on people.

I've been developing software and video games since the 90s, always with a focus in low level programming, 3D graphics and game engine development. Since 2018 I've been working mostly on algorithmic trading and created [ENZO-TS](https://www.enzobot.com), a complete trading system for cryptocurrencies.

Some pointers:
- My favorite programming language is C++ (for better or for worse), and I follow the best-practices (exceptions, `auto`, labmdas, etc.).
- I don't like weakly-typed languages. Their flexibility can quickly lead to ambiguity and bugs.
- Italian is my mother tongue, English second, Japanese a distant third.
- In 2022 I started learning Russian and Chinese on Duolingo ([my profile](https://www.duolingo.com/profile/TheCrib)).
- I have a [YouTube channel](https://www.youtube.com/c/DavidePasca), mostly about algo-trading, sometimes Duolingo lessons or programming.

## Projects

### ENZO Trading system (2018~)

A complete trading system for cryptocurrencies. See [www.enzobot.com](https://www.enzobot.com).

![](/images/20221017_tsp_with_indicators.png)

#### My work on the project

I developed most of the front-end and trading models in C++. Some of the major tasks are:

- Realized machine-learning driven trading algorithms and indicators
- Live trading on Bybit and Binance exchanges via REST and WebSocket APIs
- Backtesting infrastructure
  - Simulation of exchange orders, including HFT (sub-minute) data
  - Reporting of P&L, Calmar ratio, Sharpe ratio, Monte Carlo validation, etc.
- Risk management (see video [Levels of risk management. Our approach summarized.](https://youtu.be/09yW6IgQkqA))
- Live profit calculation and reporting
- TCP/IP client-server infrastructure to distribute trading signals to customers
- IPC protocol based on BSD sockets
- UI based on Dear ImGui
- Chart and indicators rendering in OpenGL

#### What I learned

- Challanges of building consistently profitable strategies
- Practical meachine-learning application and techniques to reduce curve fitting
- REST API connectivity and crypto exchange protocols
- Risk and portfolio management techniques
- Leverage trading and short selling
- Usage of Dear ImGui for a complex project
- Reliance on multiprocessing for fault-tolerance

### xComp image comparer (2022)

An image viewer capable of building composites of a stack of images with transparent regions. Source code at [github.com/gugenstudio/xComp](https://github.com/gugenstudio/xComp)

This tool was built to visualize region updates of a render on top of previous renders, in real-time. Images found in a chosen folder to scan for, are quickly composited with alpha blending in a stack. OpenColorIO transformations are optionally added to the composite image, which can be saved out as a PNG.

![](https://raw.githubusercontent.com/gugenstudio/xComp/master/apps/docs/xcomp_sshot_01.jpg)

#### My work on the project

I was the sole developer on this project. The main tasks were:

- Setting up an multi-platform UI infrastructure with Dear ImGui and GLFW
- Implementation and use of OpenEXR and OpenColorIO
- Image compositing with alpha blending and resampling
- UI to manage EXR layers and masks

#### What I learned

- Build and usage of OpenEXR and OpenColorIO

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
