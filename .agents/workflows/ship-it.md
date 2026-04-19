---
description: Finalize code, verify performance, and deploy.
---

1. **Call @CoreDeveloper**: Run @verification-before-completion to ensure the app builds and tests pass.
2. **Performance Audit**: Use @vercel-react-native-skills to check for list optimizations (FlashList) and bundle size.
3. **Call @QualityGuardian**: Execute the @requesting-code-review skill. The agent must provide a 🔴/🟡/🔵 report.
4. **Fix Issues**: Address all 🔴 (Critical) issues automatically.
5. **Deployment**: Use @expo-deployment and @expo-cicd-workflows to trigger an EAS Build.