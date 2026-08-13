CSS preprocessors extend plain CSS with features that CSS itself lacked for years -- variables, nesting, mixins, functions, and partials. They compile down to standard CSS that every browser understands.

- CSS Preprocessors
  - What is a preprocessor? 🔴
    - Write in a superset of CSS -> compile to plain CSS
    - Adds variables, nesting, mixins, functions, math
  - Why use a preprocessor?
    - DRY (Don't Repeat Yourself)
    - Better organization (partials, imports)
    - Maintainable themes (variables)
    - Cross-browser support (vendor prefixes)
  - Popular preprocessors
    - [Sass / SCSS](./SASS/README.md) 🔴 -- the most popular
    - Less
    - Stylus
    - PostCSS (technically a post-processor, but similar role) 🔴
  - Sass vs Less vs Stylus 🔴
    - Sass/SCSS: most popular, two syntaxes (`.sass` indented, `.scss` CSS-like)
    - Less: JavaScript-based, popular with older Bootstrap
    - Stylus: very concise, optional braces/colons
  - Modern CSS has caught up 🔴
    - CSS now has custom properties (`--var`), nesting, `@layer`
    - But preprocessors still offer mixins, loops, and better tooling
  - Build integration 🔴
    - Vite, Webpack, Parcel compile Sass/Less automatically
    - `npm install -D sass`
  - [Sass / SCSS](./SASS/README.md) (covered in detail)

---
🔴 Very Important
