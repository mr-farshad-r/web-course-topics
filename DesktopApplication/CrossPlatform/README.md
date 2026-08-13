Cross-platform desktop development means writing a single codebase that produces a working application on Windows, macOS, and Linux. The dominant approach today uses web technologies (HTML/CSS/JavaScript) inside a native runtime like Electron or Tauri.

- Cross-Platform Desktop
  - What is cross-platform desktop? 🔴
    - One codebase -> Windows, macOS, Linux binaries
    - Usually web tech inside a native shell
  - [Electron](./Electron/README.md) 🔴 -- the most popular option
  - Alternatives 🔴
    - **Tauri** 🔴 (Rust backend + web frontend, much smaller binaries)
    - **Flutter Desktop** (Dart, single codebase incl. mobile)
    - **.NET MAUI** (C#, Microsoft)
    - **Qt** (C++, mature, industrial)
  - Comparison 🔴
    - Electron: biggest ecosystem, easiest for web devs, large binaries (~100MB)
    - Tauri: tiny binaries (~10MB), Rust backend, uses system WebView
    - Flutter: same language as mobile, custom rendering
  - Shared concepts
    - Main process vs renderer process (Electron) 🔴
    - IPC (Inter-Process Communication) 🔴
    - Native menus, tray, dialogs
    - File system access
    - Auto-update
    - Code signing and notarization 🔴
  - Choosing a framework 🔴
    - Know React/Vue/JS -> Electron or Tauri
    - Already using Flutter for mobile -> Flutter Desktop
    - Enterprise C# -> .NET MAUI
  - When NOT to go cross-platform
    - Need peak native performance (games, video editing) -> Native
    - Tiny utility where even 50MB is too big -> Tauri or native

---
🔴 Very Important
