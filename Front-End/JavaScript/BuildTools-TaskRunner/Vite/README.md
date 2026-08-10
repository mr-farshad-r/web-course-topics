Vite is the modern, lightning-fast build tool created by Evan You (the creator of Vue). It uses esbuild for development (near-instant startup) and Rollup for production builds, and has become the default choice for new React, Vue, and Svelte projects.

- Vite
  - Introduction 🔴
    - What Vite is (dev server + bundler)
    - Native ESM dev server (no bundling in dev)
    - Why it's so fast 🔴
      - esbuild for dependency pre-bundling (Go, 10-100× faster than Babel)
      - On-demand compilation
      - Rollup for production
  - Installation / scaffolding 🔴
    - `npm create vite@latest`
    - Templates: React, Vue, Svelte, Preact, Lit, Vanilla
    - TypeScript support out of the box
  - Development
    - `npm run dev` -- starts dev server in milliseconds
    - HMR (Hot Module Replacement) over native ESM 🔴
    - No full reload needed for most changes
  - Production build
    - `npm run build` -- Rollup under the hood
    - `npm run preview` -- preview the production build
  - Configuration (`vite.config.ts`) 🔴
    - ```js
      import { defineConfig } from 'vite'
      import react from '@vitejs/plugin-react'

      export default defineConfig({
        plugins: [react()],
        server: { port: 3000, proxy: {...} }
      })
      ```
  - Plugins 🔴
    - `@vitejs/plugin-react`
    - `@vitejs/plugin-vue`
    - `vite-plugin-pwa`
    - Compatibility with Rollup plugins
  - Features
    - CSS / CSS Modules / Sass / PostCSS support
    - Static asset handling
    - Environment variables (`import.meta.env`)
    - Glob imports
    - Worker support
  - Path aliases (`resolve.alias`)
  - Dev server proxy 🔴 (avoid CORS in dev)
  - SSR support
  - Library mode (build a component library)
  - Vite vs Webpack 🔴
    - Vite: faster dev, simpler config, modern default
    - Webpack: more mature, more plugins, legacy projects
  - When to use Vite 🔴
    - Any new React/Vue/Svelte project
    - Migrating away from Create React App

---
🔴 Very Important
