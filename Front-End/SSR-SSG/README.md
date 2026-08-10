SSR (Server-Side Rendering) and SSG (Static Site Generation) are two strategies for rendering web pages on the server instead of entirely in the browser. They improve performance, SEO, and first-contentful paint compared to a pure client-side SPA.

- SSR / SSG
  - Rendering strategies 🔴
    - CSR (Client-Side Rendering) -- classic SPA
    - SSR (Server-Side Rendering) -- HTML generated per request
    - SSG (Static Site Generation) -- HTML generated at build time
    - ISR (Incremental Static Regeneration)
    - Hydration (making server HTML interactive on the client) 🔴
  - Why bother? (SEO, FCP/LCP, social sharing previews)
  - Trade-offs
    - CSR: rich interactivity, poor SEO, slow first paint
    - SSR: good SEO, server cost, TTFB matters
    - SSG: fastest, best for content sites, rebuild on change
  - Meta-frameworks 🔴
    - Next.js (React)
    - Nuxt.js (Vue)
    - SvelteKit (Svelte)
    - Astro (islands)
    - Gatsby (GraphQL + SSG)
  - Key concepts
    - `getServerSideProps` / `getStaticProps` / `getStaticPaths` (Next.js)
    - App Router vs Pages Router
    - Server Components (React 18+)
  - [Next.js](./NEXTjs/README.md)

---
🔴 Very Important
