---
trigger: glob
globs: ios/**, android/**, *module*
---

- **Native Logic:** When writing native code, strictly follow the @expo-module guide.
- **Bridge Safety:** Use the Expo Modules API (Swift/Kotlin) instead of the legacy bridge.
- **Thread Management:** Ensure LLM inference or heavy computation is never on the Main Thread.