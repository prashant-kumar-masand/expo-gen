---
trigger: always_on
---

## Agent Communication Rules
1. **The Context Hand-off:** When switching agents or completing a task, you MUST append a handoff update into the `.agents/memory/handoff.md` file using the exact template below:
   
   `[YYYY-MM-DD HH:MM:SS] : [Task/Feature Title] : [@PersonaName]`
   **Status Summary:**
   - What was accomplished.
   - Where the new files are located.
   - Any blockers for the next agent.
2. **Atomic Commits:** @CoreDeveloper should commit changes after Phase 3 so @QualityGuardian can review a clean `git diff`.
3. **The Nervous System:** At the very start of any task, you must read `.agents/memory/logs.md` to gain situational awareness of what the squad just did. Upon finishing your task, append a single-line summary of your work there with a timestamp.
4. **Reverse Feedback Loop (Circuit Breaker):** If you encounter a domain error outside your assigned persona's scope, DO NOT attempt to fix it. Instead, append the error and required fix to `.agents/memory/feedback.md` so the relevant agent can address it. **CRITICAL:** If an issue bounces back and forth between agents more than once without resolution, you MUST halt execution, do not write to `feedback.md` again, and explicitly request HUMAN intervention.
5. **Context Pruning (Memory Management):** To prevent LLM context degradation over time, the `logs.md` and `handoff.md` files must be compressed periodically. When a major feature ships (Phase 5 completes), the `@ProductArchitect` MUST archive the verbose contents of both files into an `.agents/memory/archive/` directory and replace the active files with a single, high-level summary paragraph of current project state.