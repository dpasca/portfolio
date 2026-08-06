[OVERSWEEP](https://oykgames.com/oversweep) is an accessible carrier-interceptor combat flight game, written in C++20 on a native Vulkan renderer and headed for a commercial release on Steam. I am the sole developer. It is currently a playable multi-mode vertical slice: authored operations, free flight, tutorials, and deterministic demos running over one fixed-step simulation, flying a variable-sweep carrier interceptor inspired by the F-14D.

The project stands directly on [XPSVR](#xpsvr-experimental-flight-simulator). That earlier simulator is where I learned flight dynamics, missile guidance, autopilot, avionic displays, and what a cockpit has to do before an aircraft feels flown. OVERSWEEP inherits almost none of its code and nearly all of that judgement. The renderer is new and the platform is new, but the hard questions are ones I have already answered once, which is precisely what makes it possible to answer them quickly now.

The other half is working effectively with AI agents. [Little Control Room](#little-control-room) is the tool I built for that, and OVERSWEEP is its heaviest user: many concurrent worktrees, agent sessions, runtimes, and review loops on a single project, coordinated from one place. Experience decides *what* to build and what "correct" means; the agents and LCR decide how quickly a decision becomes working, tested code.

That pairing is the goal of the project, and also the reason why I was willing to undertake it. A flight simulator can be a very demanding project, because there is almost no end to realism and it's very easy to get lost in a myriad of details, many of which require careful research. Without advanced AI tooling, this would be too time consuming for an individual with little free time.

#### The cockpit is a text file

Every panel, instrument frame, canopy arch, and switch is declared in a readable text description of boxes, lofts, arcs, materials, mirroring, and articulation. The build turns it into a mesh, while a live workbench lets me nudge primitives and write changes back without reformatting the source. Changing a canopy radius is therefore one edit, not a remodel. The shell rebuilds in place, so the effect is visible immediately without a modelling package in the loop.

Smoothing, contact occlusion, wear, and grime are regenerated from the geometry, so they cannot go stale. The procedural pilot is posed from the same fitted anchors: move a throttle and the hand follows. A second aircraft becomes another modular description rather than another modelling pipeline.

<div class="project-gallery project-gallery--two project-gallery--cinema">
  <figure>
    <img src="{{ site.baseurl }}/images/oversweep-cockpit-forward.jpg" loading="lazy" alt="OVERSWEEP cockpit forward view with instruments and multifunction displays">
    <figcaption>The procedural cockpit, built entirely from a text description: canopy arcs, mechanical instruments, and live typed displays.</figcaption>
  </figure>
  <figure>
    <img src="{{ site.baseurl }}/images/oversweep-break-turn.jpg" loading="lazy" alt="OVERSWEEP aircraft in a loaded break turn with afterburners lit">
    <figcaption>A loaded break off the carrier pass, over the analytic sea with gravity-wave normals and screen-space reflections.</figcaption>
  </figure>
</div>

#### My work on the project

I am the sole developer. The main areas of work include:

- Native SDL3/Vulkan forward renderer with reversed-infinite depth, cascaded and player shadow maps, SSAO, HDR and bloom, environment SH plus GGX specular IBL, clouds, and a shared analytic sea with gravity-wave normals and screen-space reflections
- Real-world terrain from Copernicus GLO-30 elevation data in UTM metre space: adaptive topology, connected-ocean classification, GEBCO bathymetry, land-cover chroma, and a 70 × 100 km playable region around the Strait of Hormuz
- The procedural cockpit description format, its mesh builder, the live layout workbench with comment-preserving write-back, the contact-occlusion bake, and the derived wear atlas
- A procedural pilot body posed from the fitted seated anchors, with hands and boots rigidly attached to the stick, throttle, and rudder pedals
- Gameplay flight model with energy exchange, automatic wing sweep and manoeuvre devices, landing flaps and gear, and pilot G physiology
- A typed avionics bus feeding the HUD combiner, VDI, HSD, TSD, multifunction displays, and six mechanical flight instruments, so no display state is invented in the renderer
- Weapon systems: a product-owned infrared seeker, guidance, launch envelope, and gun
- Mission and operations shell: intercepts, identification and weapons-hold scenarios, free flight, and a guided runway landing tutorial with continuous coaching and a scored debrief
- Audio combining typed procedural layers with authored jet and radar-intercept-officer assets, and a data-driven instructor voice
- Determinism as a working tool: tick-addressed input replay, fixed-clock screenshot capture, golden images, and measured PSNR comparison floors
- Steam-first packaging on Windows, with macOS as the daily development platform and Linux, Proton, and mobile kept as portability boundaries

#### What I learned

- Thirty years of graphics and simulation experience compounds differently now: the scarce skill is deciding what is correct and how to verify it, not typing the implementation
- Agents are only as good as the evidence loop around them. Deterministic captures, pinned invariants, and measured noise floors turn "looks fine" into a number you can argue with
- Procedural, source-owned assets suit AI-assisted development far better than binary art: a text description is reviewable, diffable, testable, and cheap to regenerate
- Writing decisions down is what stops many parallel agent sessions from quietly contradicting each other; the project carries over a hundred architecture decision records for that reason
- Speed at this scale comes from tooling rather than typing, which is why building [Little Control Room](#little-control-room) first paid for itself here
