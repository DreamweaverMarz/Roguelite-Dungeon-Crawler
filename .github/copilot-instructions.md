# Copilot Instructions for Dungeon Crawler Project

## Project Overview
This is a side scrolling roguelite dungeon crawler developed in Unity 3D using the Corgi Engine by More Mountains. The project is written in C#, structured around modular scenes, procedurally generated levels, and tight combat mechanics.

## Code Style Guidelines
- Use Unity C# conventions (PascalCase for methods/classes, camelCase for variables).
- Prefer scriptable objects for configuration and decoupling.
- Use public methods sparingly; favor `[SerializeField] private` with property accessors if needed.
- Avoid `Update()` unless necessary. Prefer events or coroutines.
- Follow the component-driven design encouraged by Corgi Engine.

## Gameplay System Conventions
- Core loop: explore, fight, collect, upgrade, die, repeat.
- Use the Corgi Engine’s Character Abilities framework for movement and combat.
- Game systems (combat, inventory, health) must be modular and extensible.
- Randomness must be seeded and testable (e.g., procedural generation).
- Use finite state machines for enemy AI and player state logic.
  
## Documentation & PRDs
- When writing design docs (PRDs), use this format:
  - **Overview**
  - **Player Experience Goals**
  - **Features / Mechanics**
  - **Technical Requirements**
- Output in Markdown, with bullet points or headers when appropriate.

## Development Practices
- All changes must be made in branches and submitted via pull requests.
- Include relevant class and method summaries using XML documentation comments.
- When editing existing systems, summarize the impact in comments or commit messages.
- Avoid monolithic scripts — break logic into separate responsibilities.

## Prompt Behavior
- Prefer short, clean responses unless asked for long-form content.
- Always assume the user is building in Unity with Corgi Engine.
- Never reference MonoBehaviours or Unity APIs that aren’t compatible with the current Unity LTS version.
- When generating code, include `[Header("Your Header Here")]` attributes for serialized fields to improve inspector clarity.

