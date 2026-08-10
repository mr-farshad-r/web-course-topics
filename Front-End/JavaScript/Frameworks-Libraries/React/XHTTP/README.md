Almost every React application needs to talk to a server -- to fetch data, submit forms, or stream updates. This section covers the libraries and patterns for making HTTP (XHTTP) requests from React.

- XHTTP Requests in React
  - Why we need data fetching in React
  - Where to fetch (useEffect vs event handlers vs libraries)
  - **Fetch API** 🔴
    - Native browser API, no install needed
    - Basic usage
      - ```js
        fetch('/api/users')
          .then(res => res.json())
          .then(data => setUsers(data))
        ```
    - Async/await syntax 🔴
    - Error handling (`try/catch` or `.catch()`)
    - Request options: method, headers, body
    - AbortController (cancel requests) 🔴
  - **Axios** 🔴
    - `npm install axios`
    - Why Axios over Fetch
      - Automatic JSON parsing
      - Request/response interceptors
      - Timeouts
      - Better error objects
      - Wide browser support
    - Basic usage
      - `axios.get('/api/users')`
      - `axios.post('/api/users', data)`
    - Instance and defaults 🔴
      - `axios.create({ baseURL, headers })`
      - Interceptors (auth tokens, logging)
    - Handling loading / error / data states
  - Fetching patterns in components 🔴
    - Fetch on mount (`useEffect`)
    - Fetch on user action (button click)
    - Loading state
    - Error state
    - Race conditions and cleanup 🔴
  - CORS 🔴
    - What it is and why browsers enforce it
    - Preflight (`OPTIONS`) requests
    - Fixing CORS (server-side, not client)
  - File Upload 🔴
    - Multipart/form-data
    - Progress tracking with Axios
  - **React Query / TanStack Query** 🔴
    - The modern way to fetch in React
    - Caching, dedup, background refresh
    - `useQuery`, `useMutation`
    - DevTools
  - SWR (by Vercel) -- alternative to React Query
  - GraphQL clients
    - Apollo Client
    - urql
  - Server-Sent Events (SSE) and WebSockets
  - Authentication 🔴
    - Bearer token in `Authorization` header
    - Refresh token flow
  - Best practices 🔴
    - Centralize API calls (service layer)
    - Type responses (TypeScript interfaces)
    - Handle loading and error UI states
    - Cancel in-flight requests on unmount

---
🔴 Very Important
