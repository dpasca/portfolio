---
---
RogueLLM is an experimental roguelike that combines traditional dungeon crawling with LLM-generated worlds. The player can request almost any setting, from a one-word theme to a detailed premise, and the system generates locations, enemies, items, and narrative flavor around that theme.

The current gameplay focuses on exploration, combat, equipment, and inventory management, with generated world descriptions and events providing the texture around the mechanics.

#### My work on the project

I built the prototype and have continued updating it as an AI-gameplay experiment. Major tasks include:

- Python web application for launching and playing generated roguelike sessions
- LLM-driven world generation for settings, locations, enemies, items, and descriptions
- Combat, inventory, equipment, health, attack, XP, and location-state systems
- Theme input flow that can turn short prompts or longer setting descriptions into playable worlds
- Search-provider support for enriching generated game descriptions when useful
- Seeded development worlds for repeatable local testing and smoke checks
- Browser UI for map navigation, character status, inventory, and event log display

#### What I learned

- LLMs are strongest in games when they provide variety and flavor while deterministic systems protect playability
- Generated content needs caching, validation, and repeatable seeds to stay debuggable
- Even simple mechanics feel richer when the generated theme changes the player's expectations
- AI games need a careful boundary between improvisational text and stable game-state rules
