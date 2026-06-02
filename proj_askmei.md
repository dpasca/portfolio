---
---
[AskMei.ai](https://askmei.ai) is a modern AI assistant built on the ChatNext3 platform. It combines multi-model LLM routing, live web search, image generation, memory, file and vision support, and a friendly skeuomorphic interface into a single web/PWA experience.

The system is designed as a multi-instance platform: the same codebase can ship different branded assistants with their own prompts, visual identity, model choices, pricing, rewards, and deployment settings.

AskMei was developed with modern AI coding tools as part of the everyday engineering workflow, including implementation, review, visual iteration, and release work.

<div class="project-gallery project-gallery--two project-gallery--portrait">
  <figure>
    <img src="{{ site.baseurl }}/images/askmei-chat-portrait.jpg" alt="AskMei mobile chat interface">
    <figcaption>Regular chat interface in the Spring Canopy theme.</figcaption>
  </figure>
  <figure>
    <img src="{{ site.baseurl }}/images/askmei-home-hero-portrait.jpg" alt="AskMei home page hero artwork">
    <figcaption>Mei's warm visual identity for the public-facing experience.</figcaption>
  </figure>
</div>

#### My work on the project

I designed and implemented the product, front-end, backend, AI orchestration, deployment, and monetization systems. Major areas include:

- Multi-model assistant architecture with a backend preparation agent, model routing, tool orchestration, and a user-facing response model
- Tool system for live web search, link scraping, image generation, calendar and memory retrieval, user context, and HTML artifact generation
- Editable memory system with compact summaries, detailed YAML memory, user import/export, and background consolidation
- File, image, and PDF handling so the assistant can reason over uploaded content
- Skeuomorphic visual design, including the "Spring Canopy" desk interface and themed assistant presentation
- Credits, subscriptions, power packs, daily rewards, and optional ad-based credit earning
- Multi-instance configuration for branded deployments such as AskMei and other specialized assistants
- PWA support and Capacitor groundwork for iOS and Android packaging
- Production deployment, observability, authentication, and payment integration

#### What I learned

- How to separate model preparation, tool use, and final response generation without overloading a single assistant prompt
- How to balance quality, latency, and cost through model routing and selective tool use
- How much control users need around memory for an assistant to feel useful rather than intrusive
- How visual identity changes the perceived warmth and usability of an AI product
- How to build an AI assistant as an adaptable product platform rather than as a single fixed chatbot
