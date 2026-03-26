# TypeScript Config

Shared TypeScript configurations.

## Presets

| Preset | Export | Use for |
|--------|--------|---------|
| **Base** | `@repo/typescript-config/base.json` | Packages, libraries (NodeNext resolution) |
| **App** | `@repo/typescript-config/app.json` | React Router / Vite apps (Bundler resolution, `react-jsx`) |
| **Playwright** | `@repo/typescript-config/playwright.json` | E2E test suites |

## Usage

```json
{
  "extends": "@repo/typescript-config/app.json",
  "compilerOptions": {
    "paths": {
      "@/*": ["./*"],
      "@ui/*": ["../../packages/design-system/src/*"],
      "@palette/*": ["../../packages/palette/src/*"]
    }
  }
}
```

For libraries/packages:

```json
{
  "extends": "@repo/typescript-config/base.json",
  "compilerOptions": {
    "jsx": "react-jsx"
  }
}
```
