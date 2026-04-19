---
description: Create a custom Expo Module for native iOS/Android features.
---

1. **Call @CoreDeveloper**: Use @expo-module to scaffold a new native module.
2. **Environment Check**: Use @expo-dev-client to ensure the development build is ready for native code.
3. **Write Swift/Kotlin**: Implement the native logic, following the safety rules in @native-safety.md.
4. **JS Wrapper**: Create the TypeScript interface for the module.
5. **Verify**: Use @verification-before-completion to build the local dev client and test the module.