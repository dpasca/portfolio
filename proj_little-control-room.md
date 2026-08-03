[Little Control Room](https://github.com/dpasca/LittleControlRoom) is a terminal-first control center for my AI-heavy development workflow. It keeps work across many repositories, agent sessions, TODOs, diffs, and project runtimes in one place. It is now the main tool I use to develop and coordinate my other projects, including AskMei.ai, Fractal Strike, and RogueLLM. Its heaviest user is [OVERSWEEP](#oversweep), where many concurrent worktrees, agent sessions, and runtimes run against one codebase at once.

One of my main lessons from using AI agents is to use them to build better tools for the way we work. Personal tools remove very specific friction and keep more of the workflow under my control when a vendor changes direction. LCR therefore works with Codex, Claude Code, and OpenCode rather than being designed around a single provider or harness.

Creating LCAgent, an experimental coding agent native to LCR, is an important next step. It is both research into where the model ends and the harness begins, and a practical move toward independence. It does not remove reliance on external models, but moves that reliance down a layer: from one complete coding-agent product to replaceable LLMs behind tools and policies I control.

That exposes the less visible challenges of agent engineering: choosing and compacting context without losing important state, resuming reliably, managing security through permissions and command vetting, preventing common destructive actions, and keeping enough trace and verification evidence to understand what happened.

<div class="project-gallery project-gallery--two project-gallery--wide">
  <figure>
    <img loading="lazy" src="{{ site.baseurl }}/images/lcr-main-panel-live-runtime.jpg" alt="Little Control Room dashboard with project status and runtime pane">
    <figcaption>Main dashboard with project status, attention signals, and a managed runtime pane.</figcaption>
  </figure>
  <figure>
    <img loading="lazy" src="{{ site.baseurl }}/images/lcr-codex-embedded-fresh.jpg" alt="Little Control Room embedded Codex session">
    <figcaption>Embedded Codex session with local context, diffs, commands, and activity visible.</figcaption>
  </figure>
</div>

#### My work on the project

I am the sole developer. The main areas of work include:

- Go-based TUI for monitoring and navigating many projects without losing sight of active agent work
- Embedded Codex, Claude Code, and OpenCode sessions, with provider-neutral project and session workflows
- TODO, Git diff, commit, worktree, conflict-resolution, and managed-runtime tools kept close to the agent sessions
- Artifact-first project and session discovery, using local state rather than requiring a central cloud service
- Boss Chat, a higher-level view for project inventory, session recall, and confirmable control proposals
- LCAgent's provider-flexible loop, durable thread state, context compaction, permission and approval policies, command guardrails, verification traces, and repeatable evaluations
- Local and API-backed inference across multiple agent tools, model providers, and OpenAI-compatible endpoints

#### What I learned

- Building tools for my own workflow creates compounding leverage and reduces dependence on any one vendor's product decisions
- Provider and harness independence has to be designed into the architecture; it is difficult to add after everything assumes one agent
- Much of an agent's intelligence comes from the model, but reliability comes from the surrounding work on context, compaction, permissions, recovery, and verification
- Security is most useful when its guarantees are explicit and narrow: vet commands, require approval where appropriate, block known dangerous actions, and remain honest about what is not sandboxed
