---
---
[Little Control Room](https://github.com/dpasca/LittleControlRoom) is a terminal-first control center for AI development work across many local repositories. It is now the main tool I use to develop and coordinate everything else, including projects such as AskMei.ai, Fractal Strike, and RogueLLM.

It keeps Codex, OpenCode, and Claude Code sessions visible, helps resume work quickly, and brings TODOs, diffs, commits, runtime processes, and project status into one place. The tool itself is also developed through the same AI-assisted workflow it is designed to supervise.

It also includes an experimental native AI engineer, LCAgent, which can run coding sessions with structured local artifacts, permissions, verification traces, and benchmark tooling.

<div class="project-gallery project-gallery--two project-gallery--wide">
  <figure>
    <img src="{{ site.baseurl }}/images/lcr-main-panel-live-runtime.jpg" alt="Little Control Room dashboard with project status and runtime pane">
    <figcaption>Main dashboard with project status, attention signals, and a managed runtime pane.</figcaption>
  </figure>
  <figure>
    <img src="{{ site.baseurl }}/images/lcr-codex-embedded-fresh.jpg" alt="Little Control Room embedded Codex session">
    <figcaption>Embedded Codex session with local context, diffs, commands, and activity visible.</figcaption>
  </figure>
</div>

#### My work on the project

I am the sole developer. The main tasks include:

- Go-based TUI for multi-project monitoring, filtering, pinning, snoozing, archiving, and attention scoring
- Artifact-first scanning of Codex, OpenCode, and Claude Code sessions across local projects
- Embedded session panes for Codex, OpenCode, and Claude Code, including resume/new flows and model selection
- Per-project TODO lists that can launch fresh AI coding sessions from selected tasks
- Git diff, image diff, commit preview, push, and conflict-resolution workflows from inside the TUI
- Managed runtime commands with run/stop/restart, output capture, port/status awareness, and project-local configuration
- Boss Chat, a high-level chat surface for project inventory, session recall, and confirmable control proposals
- LCAgent, an experimental LCR-native coding agent with provider-backed tool calls, autonomy levels, JSONL traces, verification summaries, and repeatable eval lanes
- Local and API-backed background inference through Codex, OpenCode, Claude Code, MLX, Ollama, and OpenAI-compatible APIs

#### What I learned

- Agent-heavy software work needs strong situational awareness as much as it needs better individual agents
- Local disk artifacts can be a practical source of truth for session discovery and project state
- Human control over autonomy, verification, and resumability matters more than hiding the machinery
- A TUI can be an effective control surface for complex AI workflows when the information density is carefully managed
