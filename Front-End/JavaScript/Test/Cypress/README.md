Cypress is a modern, developer-friendly end-to-end (E2E) testing framework for web applications. Unlike older tools (Selenium) that drive the browser remotely, Cypress runs inside the browser alongside your app -- making tests fast, reliable, and easy to debug.

- Cypress
  - Introduction 🔴
    - What Cypress is (E2E + component testing)
    - Runs inside the browser (not remote-driven like Selenium)
    - Real-time reloads and time-travel debugging
  - Installation 🔴
    - `npm install -D cypress`
    - `npx cypress open` (interactive mode)
  - Writing tests 🔴
    - `describe()` / `context()` -- group tests
    - `it()` / `specify()` -- define a test
    - ```js
      describe('Login', () => {
        it('logs in with valid creds', () => {
          cy.visit('/login')
          cy.get('input[name=email]').type('user@test.com')
          cy.get('input[name=password]').type('secret{enter}')
          cy.url().should('include', '/dashboard')
        })
      })
      ```
  - Core commands 🔴
    - `cy.visit(url)` -- navigate
    - `cy.get(selector)` -- query DOM
    - `.type(text)`, `.click()`, `.select()`, `.check()`
    - `.should('be.visible')`, `.should('have.text', '...')`
    - `.contains(text)`
    - `cy.request(url)` -- HTTP requests (API testing)
  - Assertions 🔴
    - Chai-style: `.should('have.length', 3)`
    - Implicit: Cypress auto-retries commands
  - Handling async (Cypress commands are queued, not Promise-based) 🔴
    - Commands are retried automatically
    - Avoid `async/await` (Cypress handles timing)
  - Fixtures 🔴
    - `cypress/fixtures/` -- test data (JSON, images)
    - `cy.fixture('users.json').then(...)`
  - Custom commands 🔴
    - `Cypress.Commands.add('login', (...) => {...})`
    - `cypress/support/commands.js`
  - Page Object Model (optional pattern) 🔴
  - Network control 🔴
    - `cy.intercept()` -- stub or spy on network requests
    - Mock API responses for deterministic tests
  - Authentication 🔴
    - `cy.session()` -- persist login across tests
    - Set token in localStorage/sessionStorage
  - Screenshots and videos 🔴
    - Automatic on failure
    - `cy.screenshot()`
  - Configuration (`cypress.config.js`) 🔴
    - `baseUrl`
    - `viewportWidth`, `viewportHeight`
    - Environment variables
  - Cypress Studio (recording tests by clicking)
  - Cypress vs Playwright vs Selenium 🔴
    - Cypress: easiest DX, Chrome/Firefox/Edge (no Safari)
    - Playwright: cross-browser (incl. Safari), modern, faster
    - Selenium: oldest, language-agnostic, remote-driven
  - CI integration 🔴
    - `npx cypress run` (headless)
    - Record to Cypress Cloud

---
🔴 Very Important
