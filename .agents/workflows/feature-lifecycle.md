---
description: An automated end-to-end pipeline from brainstorming to verified code.
---

# 🚀 Workflow: Feature Lifecycle Orchestrator

## Phase 1: Requirement Discovery
- **Action:** Dispatch **@ProductArchitect**
- **Skill:** `brainstorming`
- **Goal:** Interview the user. Define the `USER_INTENT` and output a `REQUIREMENTS.md`.
- **Exit Condition:** User provides a "LGTM" on the requirements.

## Phase 2: Design & UI Implementation
- **Action:** Dispatch **@VisualEngineer**
- **Input:** `REQUIREMENTS.md`
- **Skills:** `ui-ux-pro-max`, `expo-tailwind-setup`
- **Goal:** Scaffold the components and styling. 
- **Exit Condition:** Screens are created in `src/components` with 100% Tailwind v4 compliance.

## Phase 3: Logic & Native Integration
- **Action:** Dispatch **@CoreDeveloper**
- **Input:** Visual components and `REQUIREMENTS.md`
- **Skills:** `expo-module`, `vercel-react-native-skills`
- **Goal:** Connect the UI to local LLM logic, APIs, or native modules.
- **Exit Condition:** Functional logic is implemented and `verification-before-completion` passes locally.

## Phase 4: Quality Gate
- **Action:** Dispatch **@QualityGuardian**
- **Input:** Full diff of current changes.
- **Skills:** `requesting-code-review`, `verification-before-completion`
- **Goal:** Audit the code and run a final build check.
- **Exit Condition:** No 🔴 Critical issues remain.

## Phase 5: Product Acceptance
- **Action:** Dispatch **@ProductArchitect**
- **Input:** Final app output and `.agents/memory/logs.md`
- **Goal:** Verify that the built, tested code functionally achieves all user stories defined in the initial `REQUIREMENTS.md`. Secondly, execute the "Context Pruning" rule defined in `communication.md` to clear the old logs.
- **Exit Condition:** Feature is officially approved for deployment and the memory directory is cleanly archived.

---
**Command to execute:** `/feature-lifecycle`