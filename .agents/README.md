# 🤖 ExpoGen - mobile app development multi-agent framework

Welcome to the agentic core of this project. This directory contains the definitions, personas, and specialized skills that power our autonomous development workflow for React Native and iOS.

## 👥 The Team

| Agent | Specialty | Primary Model |
| :--- | :--- | :--- |
| **@ProductArchitect** | Discovery, Spec Writing, CI/CD Planning | Claude 4.6 Opus |
| **@VisualEngineer** | UI/UX, Tailwind v4, Native Animations | Gemini 3 Flash |
| **@CoreDeveloper** | Logic, Native Modules, API Integration | Claude 4.6 Sonnet |
| **@QualityGuardian** | Code Review, Build Verification, QA | Gemini 3.1 Pro |

---

## 🛠️ Folder Structure

.agents/
├── agents.md                  # Central registry (4 agents, models, skills)
├── ProductArchitect.md        # Opus — discovery, schema ownership, boot seq
├── VisualEngineer.md          # Flash — UI/UX, styling constraints, boot seq
├── CoreDeveloper.md           # Sonnet — logic, native modules, boot seq
├── QualityGuardian.md         # Gemini Pro — review, testing, boot seq
├── README.md                  # Full docs + validation coverage table
├── memory/
│   ├── handoff.md             # Baton pass between agents
│   ├── logs.md                # Global activity log (nervous system)
│   └── feedback.md            # Cross-agent bug escalation queue
├── rules/
│   ├── communication.md       # Handoff templates, escalation protocol
│   ├── architecture.md        # Enforced folder map + types convention
│   ├── global-styles.md       # Tailwind v4, SafeAreaView, performance
│   └── native-safety.md       # Main thread safety, Expo Modules API
└── workflows/
    ├── feature-lifecycle.md   # 5-phase end-to-end pipeline
    ├── add-native-capability.md
    └── ship-it.md


- `/skills/`: Specialized "how-to" manuals that agents can load into context (e.g., `expo-module`, `ui-ux-pro-max`).
- `/rules/`: Persistent behavioral guardrails (e.g., `architecture.md`, `communication.md`, `global-styles.md`).
- `/workflows/`: Executable multi-agent sequences (e.g., `feature-lifecycle.md`, `ship-it.md`).
- `/memory/`: Dynamic state files written by agents during work:
  - `handoff.md` — Chronological task handoff log between agents.
  - `logs.md` — Global activity log (the "Nervous System").
  - `feedback.md` — Cross-agent escalation and bug queue.
- `agents.md`: The central registry mapping models to persona files.
- `*.md`: Individual persona files containing specific agent instructions (e.g., `CoreDeveloper.md`).

---

## 🚀 Common Workflows

To trigger an automated sequence, use the following commands in the Antigravity Chat:

### 1. New Feature Discovery & Design
`@ProductArchitect /new-feature [Your Idea]`
> This triggers the `brainstorming` skill to create a `REQUIREMENTS.md`, which is then passed to `@VisualEngineer` for UI scaffolding.

### 2. Native Module Development
`@CoreDeveloper /add-native-capability [Description]`
> Triggers the `expo-module` skill to scaffold Swift/Kotlin code and the `expo-dev-client` setup.

### 3. Production Readiness Check
`@QualityGuardian /ship-it`
> Triggers a chain of `requesting-code-review` and `verification-before-completion` to ensure the app is stable for deployment.

---

## 📏 Core Rules for Humans

1. **Context Hand-off:** When manually asking an agent to take over, always mention the relevant files (e.g., *"@CoreDeveloper, please implement logic for the UI created in `src/components/Login.tsx`"*).
2. **Skill Updates:** If you add a new dependency (e.g., a new charting library), update the relevant skill in `.agents/skills/` so the agents know how to use it.
3. **Model Toggling:** While agents have default models assigned in `agents.md`, you can override them in the Agent Manager if you need deeper reasoning (Opus) or higher speed (Flash).

---

## 🩺 Diagnostics

If the agents are behaving unexpectedly, run:
`@system reload-agents`
`@system status --agents`

---

## ✅ Framework Validation Coverage

| Scenario | Covered By |
| :--- | :--- |
| Cold-start agent has no context | 🚀 Boot Sequence in all 4 personas |
| Agent finishes work, next agent is lost | 📝 `handoff.md` + `communication.md` Rule 1 |
| Agent needs global situational awareness | 🧠 `logs.md` + `communication.md` Rule 3 |
| Agent finds a bug outside its domain | 🔄 `feedback.md` + `communication.md` Rule 4 |
| Agents create files in wrong locations | 🗺️ `architecture.md` + Global Constraint 4 |
| Schema/type drift between agents | 📦 `src/types/` convention + ProductArchitect Rule 4 |
| Rogue package installations | 🔒 Package constraints on ProductArchitect + VisualEngineer |
| Magic number / inconsistent styling | 🎨 VisualEngineer Styling Constraint |
| Code ships without tests | 🧪 QualityGuardian Testing Protocol (Rule 4) |
| Code builds but logic is wrong | ✅ Phase 5: Product Acceptance |
| Native code on main thread | ⚡ `native-safety.md` Rule 3 |
| Model names out of sync | 🔄 All synced: `agents.md` ↔ personas ↔ `README.md` |
| Infinite escalation loops | 🛑 Circuit Breaker in `communication.md` (Rule 4) |
| LLM Context window bloat over time | 🧹 Context Pruning in `communication.md` (Rule 5) |