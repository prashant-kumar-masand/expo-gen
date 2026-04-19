# 🗺️ Project Architecture & File System Map

All agents MUST strictly adhere to this file placement map when generating, moving, or refactoring code. Do not stray from this structure.

## React Native / Expo Route Map

```text
/
├── app/                  # Expo Router - File-based routing (pages/screens)
│   ├── _layout.tsx       # Root layout
│   ├── index.tsx         # Home screen
│   └── (auth)/           # Route groups
├── src/                  # Core application code
│   ├── components/       # Reusable UI components (buttons, cards, forms)
│   ├── hooks/            # Custom React hooks
│   ├── types/            # Shared TypeScript interfaces (barrel exported via index.ts)
│   ├── store/            # Global state (Zustand, TanStack Query)
│   ├── services/         # API calls, Antigravity local model logic
│   ├── utils/            # Helper functions
│   └── constants/        # Theme, colors, config
├── assets/               # Images, fonts
├── ios/                  # Native iOS code (Expo Modules)
└── package.json          # Project dependencies
```

## Rules:
- UI Components must ALWAYS go in `src/components/`, never in `app/`.
- Routes/Screens must ALWAYS go in `app/`.
- Custom hooks go in `src/hooks/`.
- Any local AI logic (LiteRT) goes in `src/services/ai/`.
- All shared TypeScript interfaces MUST go in `src/types/[feature].ts` and be re-exported from `src/types/index.ts`. Agents must NEVER define inline types — always import from `@/types`.
