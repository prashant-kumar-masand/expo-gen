# 🤖 ExpoGen - mobile app development multi-agent framework

A portable, production-ready multi-agent framework designed specifically for autonomous mobile app development using React Native and Expo. 

This repository is **not** a traditional software project. It is a highly specialized "nervous system" consisting of distinct AI personas, workflows, and strict architectural guardrails. When deployed alongside an Expo application, it orchestrates four dedicated agents (Product Architect, Visual Engineer, Core Developer, and Quality Guardian) to autonomously build, test, and ship mobile features.

---

## 📦 What's Inside?

The engine lives entirely within the `.agents/` directory, making it completely modular. You can lift and shift the `.agents` folder into any Expo app codebase to instantly give it autonomous capabilities.

- **4 Dedicated Personas:** Specialized instructions and model bindings (Claude 4.6 Opus/Sonnet, Gemini 3 Flash/Pro) tuned for distinct phases of the Software Development Life Cycle (SDLC).
- **Persistent Memory:** A locally managed state (`.agents/memory/`) that handles inter-agent handoffs, escalation logs, and context pruning to prevent LLM context-window degradation.
- **Workflow Orchestration:** End-to-end SDLC instructions (e.g., `feature-lifecycle.md`) to guide the squad from brainstorming to final QA validation.
- **Strict Guardrails:** Embedded rules enforcing absolute decoupling between UI components and Expo Router files, strict Tailwind v4 usage, and API/Type schema ownership.
- **Native iOS/Android Support:** Advanced skills injection to allow agents to generate raw Swift/Kotlin via the Expo Modules API without breaking the Main UI Thread.

## 🚀 How to Use

1. **Initialize an App:** Run `npx create-expo-app@latest` alongside this framework in the root, or simply drag the `.agents/` folder into an existing React Native monorepo.
2. **Start the Engine:** Hand off your vision to the Product Architect inside your chat window.
   ```text
   @ProductArchitect /new-feature "I want to build a feature that..."
   ```
3. **Approve & Watch:** The agents will use their internal Memory cluster to execute the `.agents/workflows/feature-lifecycle.md` pipeline, passing the baton automatically from Architect ➡️ Visual Engineer ➡️ Core Developer ➡️ Quality Guardian.

### 📖 Deeper Documentation
For full technical details on how the agent schemas are configured, skills are managed, and communication is enforced, see the [Internal Agent Documentation](.agents/README.md).
