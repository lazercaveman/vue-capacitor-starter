# Vue Capacitor Starter

Skip the boilerplate. Ship a cross-platform app to **Web**, **iOS**, and **Android** from a single Vue 3 codebase — everything wired up and ready to go.

## Why this starter?

Most Vue + Capacitor setups leave you stitching together tooling from scratch. This one doesn't. You get:

- **Vue 3 Composition API** with `<script setup>` — the modern way to write Vue
- **Capacitor 8** — deploy the same codebase to iOS, Android, and the web with native plugin access
- **Tailwind CSS v4** — utility-first styling that works everywhere
- **Pinia** — lightweight, TypeScript-first state management
- **Vue Router** — full client-side routing ready to extend
- **VueUse** — composable utilities so you're not reinventing the wheel
- **Vitest** — fast unit testing, co-located with your components
- **Oxlint + Oxfmt** — a modern, fast linter and formatter replacing ESLint/Prettier
- **TypeScript** throughout — strict types, no `any`
- **Yarn 4** — fast, deterministic installs with zero-installs support

No opinions on your backend. No CMS lock-in. Just a clean, modern foundation.

## Prerequisites

- **Node** `24.14.0` — use [fnm](https://github.com/Schniz/fnm) or [nvm](https://github.com/nvm-sh/nvm)
- **Yarn 4** — the only supported package manager (`npm` and `pnpm` are not supported)

## Quick Start

```bash
git clone https://github.com/lazercaveman/vue-capacitor-starter.git
cd vue-capacitor-starter
yarn install
yarn dev
```

The dev server starts at `http://localhost:5173`.

## Commands

```bash
yarn dev              # Start dev server
yarn build            # Type-check + production build
yarn preview          # Preview production build locally
yarn test             # Run Vitest
yarn test:ui          # Vitest with browser UI
yarn test:coverage    # Vitest with v8 coverage
yarn lint             # Oxlint
yarn lint:fix         # Oxlint with auto-fix
yarn format           # Oxfmt
yarn format:check     # Oxfmt dry-run (CI)
yarn type-check       # vue-tsc
```

## Project Structure

```
src/
├── assets/         # Global styles and static assets
├── components/     # Reusable Vue components
├── router/         # Vue Router configuration
├── stores/         # Pinia stores
├── views/          # Route-level components
├── App.vue
└── main.ts
```

## Deploying to iOS & Android

1. Build the web output:

    ```bash
    yarn build
    ```

2. Sync to the native projects:

    ```bash
    npx cap sync
    ```

3. Open in the native IDE:

    ```bash
    npx cap open ios      # Opens Xcode
    npx cap open android  # Opens Android Studio
    ```

Before your first native build, update [capacitor.config.ts](capacitor.config.ts) with your app's ID and name:

```ts
const config: CapacitorConfig = {
  appId: 'com.yourcompany.yourapp',
  appName: 'Your App Name',
  webDir: 'dist',
};
```

See the [Capacitor docs](https://capacitorjs.com/docs) for platform-specific environment requirements (Xcode, Android Studio, CocoaPods).

## Contributing

PRs and issues are welcome. Open an issue first for larger changes so we can align on direction before you invest the time.
