Build tools and task runners automate the repetitive work of modern front-end development: bundling modules, transpiling modern JS/TS, minifying, optimizing assets, and running dev servers. They are the pipeline between your source code and what the browser downloads.

- Build Tools and Task Runners
  - Why we need build tools 🔴
    - Bundling ES modules
    - Transpiling JSX / TypeScript / modern JS
    - Minification and compression
    - Asset optimization (images, fonts)
    - Dev server with Hot Module Replacement (HMR) 🔴
  - Task runners vs bundlers 🔴
    - Task runner: runs scripts (npm scripts, Gulp)
    - Bundler: resolves imports and produces output bundles (Webpack, Vite, Parcel, Rollup, esbuild)
  - [Webpack](./Webpack/README.md) 🔴 -- the classic, powerful, complex bundler
  - [Vite](./Vite/README.md) 🔴 -- the modern default (esbuild + Rollup)
  - [Parcel](./Parcel/README.md) -- zero-config bundler
  - [NPM Scripts](./NpmScrips/README.md) 🔴 -- the simplest task runner
  - Other notable tools
    - Rollup (libraries)
    - esbuild (blazing fast transpiler/bundler)
    - SWC (Rust-based, used by Next.js)
    - Turbopack (Vercel, Rust-based, Next.js)
  - Concepts across all tools 🔴
    - Entry point
    - Output bundle(s)
    - Loaders / transformers
    - Plugins
    - Source maps 🔴
    - Tree shaking 🔴 (dead code elimination)
    - Code splitting 🔴 (lazy loading)
    - HMR (Hot Module Replacement)
  - Choosing a build tool 🔴
    - New React project -> Vite
    - Next.js -> built-in (Webpack or Turbopack)
    - Library -> Rollup or Vite library mode
    - Zero-config -> Parcel

---
🔴 Very Important
