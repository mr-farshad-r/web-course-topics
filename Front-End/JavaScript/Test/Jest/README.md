Jest is a delightful JavaScript testing framework with a focus on simplicity. Created by Facebook (Meta), it is the default test runner for React projects and supports any JavaScript or TypeScript codebase out of the box.

- Jest
  - Introduction 🔴
    - What Jest is (all-in-one test runner, assertions, mocking)
    - Zero-config for most projects
  - Installation 🔴
    - `npm install -D jest`
    - With React: `npm install -D jest @testing-library/react @testing-library/jest-dom`
  - Writing tests 🔴
    - `test()` / `it()` -- define a test
    - `describe()` -- group related tests
    - `expect(value).toBe(other)` -- assertion
    - ```js
      test('adds 1 + 2 to equal 3', () => {
        expect(add(1, 2)).toBe(3)
      })
      ```
  - Matchers 🔴
    - `.toBe()`, `.toEqual()` (deep equality)
    - `.toBeTruthy()`, `.toBeFalsy()`, `.toBeNull()`, `.toBeUndefined()`
    - `.toContain()`, `.toHaveLength()`
    - `.toThrow()`
    - `.resolves` / `.rejects` (async/Promise)
    - `.not` (negation)
  - Setup and teardown 🔴
    - `beforeEach`, `afterEach`
    - `beforeAll`, `afterAll`
  - Mocking 🔴
    - `jest.fn()` -- mock function
    - `jest.spyOn(obj, 'method')`
    - `jest.mock('module')` -- auto-mock a module
    - Mock return values: `mockReturnValue`, `mockResolvedValue`
  - Asynchronous testing 🔴
    - `async/await`
    - `resolves` / `rejects` matchers
    - `done` callback (legacy)
  - Snapshot testing 🔴
    - `toMatchSnapshot()`
    - Good for UI components
    - Update snapshots: `jest -u`
  - Code coverage 🔴
    - `jest --coverage`
    - Statement, branch, function, line coverage
  - Configuration (`jest.config.js`) 🔴
    - `testEnvironment: 'jsdom'` (for React) vs `'node'`
    - `moduleNameMapper` (path aliases, CSS mocking)
    - `setupFilesAfterEach`
  - Running tests
    - `npm test`
    - `jest --watch` (watch mode) 🔴
    - `jest --watchAll`
    - Filter by filename or test name
  - Testing React with Jest + Testing Library 🔴
    - `render(<Component />)`
    - `screen.getByText`, `getByRole`, `getByTestId`
    - `userEvent` for interactions
    - `fireEvent` (lower-level)
  - Common patterns 🔴
    - Test behavior, not implementation
    - Avoid implementation details
    - Use `data-testid` sparingly

---
🔴 Very Important
