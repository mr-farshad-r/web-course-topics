Mobile application development is the practice of building software that runs on smartphones and tablets. There are three main approaches: **Native** (best performance and UX per platform), **Cross-Platform** (one codebase, near-native feel), and **Hybrid** (web tech inside a native wrapper).

- Mobile Application
  - Approaches 🔴
    - [Native](./Native/README.md) -- platform-specific (Swift/Kotlin)
    - [Cross-Platform](./CrossPlatform/README.md) -- one codebase, compiled to native
    - [Hybrid](./Hybrid/README.md) -- web app inside a WebView
  - Comparison 🔴
    - Performance: Native > Cross-Platform > Hybrid
    - Development speed: Hybrid > Cross-Platform > Native
    - Code reuse: Hybrid ≈ Cross-Platform > Native
    - Access to device APIs: Native > Cross-Platform > Hybrid
  - [Native](./Native/README.md)
    - [iOS](./Native/IOS/README.md) (Swift / SwiftUI)
    - [Android](./Native/Android/README.md) (Kotlin / Jetpack Compose)
  - [Cross-Platform](./CrossPlatform/README.md)
    - [React Native](./CrossPlatform/ReactNative/README.md) 🔴
    - Flutter (Dart)
  - [Hybrid](./Hybrid/README.md)
    - [Ionic](./Hybrid/Ionic/README.md)
    - Capacitor, Cordova, PhoneGap
  - Choosing an approach 🔴
    - Maximum performance / deep OS integration -> Native
    - One team, JS skills, near-native UX -> React Native
    - Content apps, existing web codebase -> Hybrid / PWA
  - Common topics across all
    - App store distribution (App Store, Google Play)
    - Push notifications
    - Offline support
    - Responsive layouts for varied screens
    - Security (secure storage, certificate pinning)
  - Progressive Web Apps (PWA) as a fourth option 🔴
    - No app store, installable from the browser
    - See [PWA](./../Front-End/JavaScript/PWA/README.md)

---
🔴 Very Important
