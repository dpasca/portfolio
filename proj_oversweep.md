[OVERSWEEP](https://oykgames.com/oversweep) is an accessible carrier-interceptor combat flight game, written in C++20 on a native Vulkan renderer and headed for a commercial release on Steam. I am the sole developer. It is currently a playable multi-mode vertical slice: authored operations, free flight, tutorials, and deterministic demos running over one fixed-step simulation, flying a variable-sweep carrier interceptor inspired by the F-14D.

The project stands directly on [XPSVR](#xpsvr-experimental-flight-simulator). That earlier simulator is where I learned flight dynamics, missile guidance, autopilot, avionic displays, and what a cockpit has to do before an aircraft feels flown. OVERSWEEP inherits almost none of its code and nearly all of that judgement. The renderer is new and the platform is new, but the hard questions are ones I have already answered once, which is precisely what makes it possible to answer them quickly now.

The other half is working effectively with AI agents. [Little Control Room](#little-control-room) is the tool I built for that, and OVERSWEEP is its heaviest user: many concurrent worktrees, agent sessions, runtimes, and review loops on a single project, coordinated from one place. Experience decides *what* to build and what "correct" means; the agents and LCR decide how quickly a decision becomes working, tested code.

That pairing is the ambition of the project. A flight simulator is an unreasonable thing to build alone at this pace, which is exactly what makes it a useful instrument: it is a real commercial product with real acceptance criteria, so the rate at which it improves is an honest reading of how fast AI tooling is genuinely getting better. Not a benchmark, a shipping deadline. The first commit is dated 12 July 2026. I expect that rate to keep rising, and this is where I will see it.

#### The cockpit is a text file

Every panel, console, instrument frame, canopy arch, and switch body is declared in a readable text description (boxes, lofts, tapered masses, elliptical arcs, materials, mirroring, repetition, articulation) which the build parses and turns into a mesh. No modelling package sits in the loop and no artist sits on the critical path. Widening the canopy arch is one edit to a radius rather than a recomputed point table, and the shell rebuilds in place inside a running developer workbench, where primitives can be nudged and committed back to the source without reformatting it.

Everything derived from that geometry is computed rather than painted: smoothing, a short-range contact-occlusion bake, and a mid-frequency wear and grime atlas. None of it can go stale when a primitive moves. The pilot's own hands, arms, and legs are procedural too, posed from the same fitted anchors, so moving a throttle grip moves the hand holding it. The practical result is that cockpits are modular: a second aircraft is a second description, not a second art contract.

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
