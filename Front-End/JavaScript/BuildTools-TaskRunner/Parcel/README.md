Parcel is a zero-configuration web application bundler. Point it at an entry HTML file and it figures out everything else -- transpilation, bundling, code splitting, asset handling -- without a config file.

- Parcel
  - Introduction 🔴
    - What Parcel is (zero-config bundler)
    - Philosophy: "just works" out of the box
  - Installation and usage 🔴
    - `npm install --save-dev parcel`
    - `npx parcel src/index.html`
    - No `parcel.config.js` needed
  - Features
    - Automatic transpilation (Babel, SWC, PostCSS)
    - Automatic dependency resolution
    - Code splitting 🔴
    - Tree shaking
    - HMR (Hot Module Replacement) 🔴
    - Image and font handling
    - SVG, GLSL, and more
  - Production build
    - `npx parcel build src/index.html`
    - Automatic minification and compression
  - Supported languages/frameworks out of the box
    - React, Vue, Svelte
    - TypeScript
    - Sass, Less, Stylus
    - GraphQL
  - Configuration (when you need it)
    - `.parcelrc`
  - Parcel vs Vite vs Webpack 🔴
    - Parcel: zero config, beginner-friendly
    - Vite: fast, modern, slight config
    - Webpack: maximum control, maximum complexity
  - When to use Parcel
    - Quick prototypes
    - Beginners who want to avoid config
    - Small to medium projects

---
🔴 Very Important
