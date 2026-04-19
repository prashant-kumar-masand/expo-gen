# 🤖 ExpoGen - mobile app development multi-agent
# Last Updated: 2026-04-19
# Framework: React Native / Expo (iOS)

---

## 🕵️ Agent: ProductArchitect
- **Role:** Requirements Engineering & System Design.
- **Model:** claude-4-6-opus
- **Persona File:** ./ProductArchitect.md
- **Active Skills:** - brainstorming
  - expo-cicd-workflows
  - expo-deployment
- **Tool Access:** filesystem, network
- **Description:** Focuses on user intent and mapping requirements to architecture.

---

## 🎨 Agent: VisualEngineer
- **Role:** High-Fidelity UI/UX & Design Systems.
- **Model:** gemini-3-flash
- **Persona File:** ./VisualEngineer.md
- **Active Skills:** - ui-ux-pro-max
  - frontend-design
  - expo-tailwind-setup
  - building-native-ui
- **Tool Access:** filesystem
- **Description:** Owns the aesthetic and functional frontend implementation.

---

## ⚙️ Agent: CoreDeveloper
- **Role:** Full-stack Mobile & Native Logic.
- **Model:** claude-4-6-sonnet
- **Persona File:** ./CoreDeveloper.md
- **Active Skills:** - vercel-react-native-skills
  - expo-api-routes
  - expo-module
  - expo-dev-client
  - vercel-react-best-practices
- **Tool Access:** filesystem, terminal, ios-simulator
- **Description:** Implements core logic and high-performance native modules.

---

## ⚖️ Agent: QualityGuardian
- **Role:** Code Review & Compliance.
- **Model:** gemini-3.1-pro
- **Persona File:** ./QualityGuardian.md
- **Active Skills:** - requesting-code-review
  - receiving-code-review
  - verification-before-completion
- **Tool Access:** filesystem, terminal
- **Description:** Final gatekeeper for code quality and build stability.

---

## 🚦 Global Constraints & Routing
1. **Context Sharing:** Agents MUST share the `REQUIREMENTS.md` file in the project root to maintain alignment.
2. **Standardization:** All UI code must be validated against the `expo-tailwind-setup` skill before merging.
3. **Verification:** No task is complete until `QualityGuardian` verifies the build via the `verification-before-completion` protocol.
4. **Architecture:** All agents MUST strictly map their file generation to the rules defined in `.agents/rules/architecture.md`.

## 🔗 Inter-Agent Communication Protocols
1. **The Handoff:** Whenever your task is done, write a summary of what you did and explicit instructions for the next agent into `.agents/memory/handoff.md`.
2. **The Nervous System:** Always review `.agents/memory/logs.md` at the start of a conversation to establish context, and append your own accomplishments to it when finished.
3. **Escalation:** If you encounter a domain error outside your persona's scope, DO NOT fix it yourself. Log it in `.agents/memory/feedback.md` for the appropriate agent to handle.