---
trigger: always_on
---

- **Styling:** Use Tailwind CSS v4 exclusively via the @expo-tailwind-setup skill.
- **Components:** Prefer functional components. Use @building-native-ui conventions for layout.
- **Performance:** Always check @vercel-react-native-skills before finalizing UI to avoid re-render loops.
- **Safe Areas:** Every screen must implement `SafeAreaView` from `react-native-safe-area-context`.