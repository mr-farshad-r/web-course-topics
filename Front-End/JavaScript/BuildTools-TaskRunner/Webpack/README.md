Webpack is the most powerful and widely-adopted module bundler for JavaScript applications. For years it was the default build tool for React (via Create React App), Angular, and Vue, and it still powers a huge number of production builds.

- Webpack
  - Introduction 🔴
    - What Webpack does (bundles modules into static assets)
    - Why it exists (module resolution, dependency graph)
  - Core concepts 🔴
    - **Entry** -- where the build starts (`./src/index.js`)
    - **Output** -- where bundles are written (`./dist`)
    - **Loaders** -- transform non-JS files (CSS, images, TS)
      - `babel-loader` (JS/JSX transpilation)
      - `css-loader` + `style-loader`
      - `file-loader` / `asset modules`
      - `ts-loader`
    - **Plugins** -- perform actions on the bundle
      - `HtmlWebpackPlugin` (generate HTML)
      - `MiniCssExtractPlugin`
      - `DefinePlugin` (env variables)
    - **Mode** -- `development` / `production`
  - Configuration (`webpack.config.js`) 🔴
    - ```js
      module.exports = {
        entry: './src/index.js',
        output: { path, filename },
        module: { rules: [...] },
        plugins: [...],
        mode: 'production'
      }
      ```
  - DevServer 🔴
    - `webpack-dev-server`
    - Hot Module Replacement (HMR)
  - Optimization 🔴
    - Code splitting (`SplitChunksPlugin`)
    - Tree shaking (ES modules only)
    - Minification (`TerserPlugin`)
    - Source maps
  - Asset handling
    - Images, fonts, SVGs
  - Environment variables 🔴
  - Webpack 5 features
    - Module Federation (micro-frontends)
    - Asset modules (built-in, replaces file-loader)
  - Pros and cons 🔴
    - Pro: extremely configurable, huge ecosystem
    - Con: steep learning curve, slow dev server vs Vite
  - When to still use Webpack
    - Legacy CRA projects
    - Complex enterprise configs
    - Module Federation

---
🔴 Very Important
