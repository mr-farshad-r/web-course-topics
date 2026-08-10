Electron is a framework for building cross-platform desktop applications using web technologies (HTML, CSS, JavaScript). Created by GitHub for the Atom editor, it powers VS Code, Slack, Discord, Figma, and thousands of other apps.

- Electron
  - Introduction 🔴
    - What Electron is (Chromium + Node.js bundled together)
    - You build a desktop app the same way you build a web app
    - Used by VS Code, Slack, Discord, Figma (desktop), Notion
  - Architecture 🔴
    - **Main process** (Node.js) -- app lifecycle, windows, native APIs
    - **Renderer process** (Chromium) -- your UI (HTML/CSS/JS)
    - **IPC** (Inter-Process Communication) -- bridge between them 🔴
  - Installation / scaffolding 🔴
    - `npm init electron-app@latest`
    - Or `git clone electron-quick-start`
    - Electron Forge (official build/packaging tool)
  - Main process basics 🔴
    - `app`, `BrowserWindow`, `Menu`, `Tray`, `dialog`, `ipcMain`
    - ```js
      const { app, BrowserWindow } = require('electron')
      app.whenReady().then(() => {
        const win = new BrowserWindow({ width: 800, height: 600 })
        win.loadFile('index.html')
      })
      ```
  - Renderer process
    - Standard web page (HTML/CSS/JS)
    - Can use React, Vue, Svelte, or vanilla JS
    - `contextIsolation: true` (security best practice) 🔴
  - IPC (Main <-> Renderer) 🔴
    - `ipcMain.handle('channel', handler)` (Main)
    - `ipcRenderer.invoke('channel', data)` (Renderer)
    - `contextBridge` to expose safe APIs 🔴
  - Native features 🔴
    - System tray icon
    - Global keyboard shortcuts (`globalShortcut`)
    - Native menus (application menu, context menu)
    - Notifications
    - Clipboard
    - File dialogs (open/save)
    - Deep links (custom protocol)
  - Packaging and distribution 🔴
    - Electron Forge or Electron Builder
    - Output: `.exe` / MSI (Windows), `.dmg` / `.app` (macOS), `.deb` / AppImage (Linux)
    - Code signing (Windows) and notarization (macOS) 🔴
  - Auto-update 🔴
    - `electron-updater` (check for updates, download, install on restart)
  - Security 🔴
    - `contextIsolation: true`
    - `nodeIntegration: false` (don't expose Node in renderer)
    - `sandbox: true`
    - CSP (Content Security Policy)
    - Validate all IPC inputs
  - Performance 🔴
    - Electron apps use more RAM than native (bundled Chromium)
    - Mitigation: lazy loading, minimize renderer processes
  - Electron vs Tauri 🔴
    - Electron: mature, huge ecosystem, large binaries (~100MB+)
    - Tauri: Rust backend, system WebView, tiny binaries (~10MB)
  - When to use Electron
    - You know web tech and need a desktop app
    - Need deep OS integration
    - Want to ship the same app on web and desktop

---
🔴 Very Important
