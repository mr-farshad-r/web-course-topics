Forms are how users send data to your application -- logins, signups, searches, checkouts. React + a validation library lets you build forms that are accessible, type-safe, and user-friendly.

- Form Validation in React
  - Why validation matters 🔴
    - Data integrity
    - User experience (instant feedback)
    - Security (never trust client input)
  - Validation levels 🔴
    - Client-side (UX)
    - Server-side (source of truth)
  - Controlled vs uncontrolled components
  - Manual validation (DIY)
    - Track errors in state
    - Validate on submit / on change / on blur
    - Painful to scale 🔴
  - **Yup** 🔴
    - Schema-based object validator
    - Declarative syntax
    - ```js
      const schema = yup.object({
        email: yup.string().email().required(),
        age: yup.number().min(18).max(120)
      })
      ```
    - `schema.validate(data)`
    - Works with Formik and React Hook Form 🔴
  - **Joi** (by Hapi)
    - Powerful schema validation
    - More common on the Node.js back-end
    - `joi-browser` / `joi` for browser
  - **Zod** 🔴 (modern, TypeScript-first)
    - TypeScript inference from schemas 🔴
    - `z.object({ email: z.string().email() })`
    - Works great with React Hook Form and tRPC
  - Integration with form libraries 🔴
    - [React Hook Form](#) + `@hookform/resolvers` + Yup/Zod
    - [Formik] + Yup (classic combo)
  - Common validation rules
    - Required
    - Min / max length
    - Email format
    - URL format
    - Number range
    - Match another field (password confirm)
    - Pattern (regex)
    - Async validation (check if username taken)
  - Displaying errors 🔴
    - Per-field error messages
    - On blur vs on change vs on submit
    - Accessibility (`aria-invalid`, `aria-describedby`)
  - Cross-field validation
  - Server-side validation reminder 🔴
    - Client validation = convenience
    - Server validation = security

---
🔴 Very Important
