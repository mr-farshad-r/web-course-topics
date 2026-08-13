NPM Scripts are custom commands defined in the `scripts` section of `package.json`. They are the simplest, most portable, and most universal task runner in the JavaScript ecosystem -- no extra dependencies, just shell commands.

- NPM Scripts
  - Introduction 🔴
    - What npm scripts are (shell commands in `package.json`)
    - Why they're powerful (no extra tool, cross-platform-ish)
  - The `scripts` field 🔴
    - ```json
      "scripts": {
        "dev": "vite",
        "build": "vite build",
        "test": "jest",
        "lint": "eslint src/"
      }
      ```
  - Running scripts 🔴
    - `npm run <script>` (for any custom script)
    - `npm start` (alias for `npm run start`)
    - `npm test` (alias for `npm run test`)
  - Built-in shortcuts 🔴
    - `start`, `test`, `install`, `publish`
  - Pre and Post hooks 🔴
    - `prebuild` runs before `build`
    - `postinstall` runs after `npm install`
    - ```json
      "scripts": {
        "prebuild": "npm run lint",
        "build": "vite build",
        "postbuild": "echo Done"
      }
      ```
  - Chaining commands 🔴
    - `&&` (run sequentially, stop on error)
    - `&` (run in parallel, not on Windows)
    - `npm-run-all` / `concurrently` (cross-platform parallel) 🔴
  - Passing arguments 🔴
    - `npm run build -- --mode staging`
    - The `--` separator
  - Environment variables in scripts 🔴
    - `cross-env` for cross-platform env vars
    - `NODE_ENV=production vite build`
  - Lifecycle scripts
    - `prepare` (runs before publish and after install)
    - `prepublishOnly`
  - Common script patterns 🔴
    - `dev` -- start dev server
    - `build` -- production build
    - `preview` -- preview prod build
    - `lint` -- run linter
    - `format` -- run formatter (Prettier)
    - `test` -- run tests
    - `test:watch`
    - `deploy`
  - Listing available scripts
    - `npm run`
  - Best practices 🔴
    - Keep scripts small and composable
    - Use `cross-env` for env vars
    - Document non-obvious scripts
    - Prefer npm scripts over Gulp/Grunt for new projects

---
🔴 Very Important
