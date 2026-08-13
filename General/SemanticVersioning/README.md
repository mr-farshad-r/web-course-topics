Semantic Versioning (SemVer) is a version-numbering convention that communicates what kind of changes a release contains. It lets developers and automated tools decide whether an upgrade is safe — without reading the entire changelog.

- Semantic Versioning (SemVer)
  - Why versioning matters
  - The SemVer spec: **MAJOR.MINOR.PATCH** 🔴
    - `MAJOR` — breaking / incompatible API changes
    - `MINOR` — backward-compatible new functionality
    - `PATCH` — backward-compatible bug fixes
  - Rules
    - Start at `0.1.0` for initial development
    - `1.0.0` marks the first stable public API
    - Every change increments exactly one number and resets lower ones
  - Pre-release and build metadata
    - `1.0.0-alpha`, `1.0.0-beta.2`, `1.0.0-rc.1`
    - `1.0.0+20230101`, `1.0.0+build.5`
  - Version ranges in package managers 🔴
    - `^1.2.3` (caret — compatible with, allows MINOR + PATCH bumps)
    - `~1.2.3` (tilde — allows PATCH bumps only)
    - `1.2.3` (exact pin)
    - `1.x`, `>=1.2 <2.0`, `*`
    - npm/pip/composer differences
  - Lockfiles 🔴
    - `package-lock.json`, `yarn.lock`, `pnpm-lock.yaml`
    - `poetry.lock`, `composer.lock`
    - Why lockfiles belong in version control
  - Changelogs
    - Keep a Changelog format
    - Conventional Commits → automated versioning + changelog
  - Git tags for releases
    - `git tag -a v1.2.0 -m "release 1.2.0"`
  - Related: CalVer (calendar versioning: `YYYY.MM.DD`)

---
🔴 Very Important
