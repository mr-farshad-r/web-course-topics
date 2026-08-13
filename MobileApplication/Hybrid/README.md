Hybrid mobile development wraps a web application (HTML, CSS, JavaScript) inside a native container (WebView) so it can be installed from an app store and access device hardware through bridges. It is the fastest way to turn existing web skills into a mobile app.

- Hybrid Development
  - What is hybrid? 🔴
    - Web app (HTML/CSS/JS) inside a native WebView shell
    - Native container provides access to device APIs (camera, GPS, ...)
  - How it works 🔴
    - UI is rendered by the platform's WebView (essentially Chrome/Safari)
    - JavaScript bridges call native code for hardware features
    - Packaged as `.apk` / `.ipa` for app stores
  - Pros 🔴
    - One codebase (HTML/CSS/JS) for iOS + Android
    - Reuse web skills and even existing web code
    - Faster development than native
    - Web developers can build mobile apps
  - Cons 🔴
    - Performance noticeably below native
    - WebView rendering can feel less smooth
    - Limited access to newest OS features (lag behind native bridge updates)
    - Heavy animations are hard
  - Tools / Frameworks
    - [Ionic](./Ionic/README.md) 🔴 -- UI components + Angular/React/Vue
    - **Capacitor** (modern, by Ionic team -- replaces Cordova)
    - Apache Cordova / PhoneGap (older)
  - Hybrid vs Cross-Platform vs Native 🔴
    - Hybrid: WebView-based, web tech, slowest but easiest
    - Cross-Platform (React Native/Flutter): JS/Dart -> real native UI, faster
    - Native: platform code, fastest, two codebases
  - When to choose hybrid 🔴
    - Content-centric apps (news, catalogs, forms)
    - Existing responsive web app to ship quickly
    - Small team with only web skills
    - When PWA is not enough (need app store presence)
  - Modern recommendation 🔴
    - For new apps: consider Capacitor + React/Vue + a UI kit
    - Or skip hybrid and use React Native / Flutter for better UX

---
🔴 Very Important
