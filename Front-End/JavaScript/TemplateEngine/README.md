A template engine lets you generate HTML by combining a template with data. Before component-based frameworks (React, Vue), template engines were the standard way to render dynamic HTML on the server or in the browser.

- Template Engines
  - What is a template engine? 🔴
    - Template + Data = HTML
    - Logic in templates (loops, conditionals, partials)
  - Server-side vs client-side templating
  - Why template engines (still matter) 🔴
    - Server-rendered apps (Express, Django, Laravel)
    - Static site generators (Eleventy, Hugo)
    - Email templates
  - Common syntax features
    - Variables `{{ variable }}`
    - Conditionals `{{#if}}...{{/if}}`
    - Loops `{{#each items}}...{{/each}}`
    - Partials / includes
    - Helpers and filters
    - HTML escaping vs raw output 🔴
  - Popular template engines
    - [Handlebars](./Handelbars/README.md)
    - EJS (Embedded JavaScript)
    - Pug (formerly Jade)
    - Mustache (logic-less)
    - Nunjucks (Jinja2-inspired)
    - Liquid (Shopify)
    - Twig (PHP/Symfony)
    - Blade (Laravel)
    - Jinja2 (Python)
  - Handlebars vs EJS vs Pug 🔴
  - Modern context 🔴
    - React/Vue/Svelte replace client-side template engines
    - But SSR frameworks and email/static still use classic engines
  - Security 🔴
    - XSS prevention (auto-escaping)
    - Never render untrusted user input as raw HTML

---
🔴 Very Important
