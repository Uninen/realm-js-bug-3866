# Repro for realm-js issue #3866

1. Install project depenencies: `yarn install`
2. Move `.env.local.example` as `.env.local` and put in a Realm App ID
3. Run development server: `yarn dev` -- the bug is now visible in console
4. Comment out script-tag in `index.html` to make the bug disappear

## Full Traceback
```

05:54:21.520 [vite] connecting... client:180:9
05:54:21.552 [vite] connected. client:202:21
05:54:21.782 Uncaught ReferenceError: global is not defined
    <anonymous> http://localhost:3000/node_modules/.vite/realm-web.js?v=e0afb5d8:1676
realm-web.js:1676:19
    <anonymous> http://localhost:3000/node_modules/.vite/realm-web.js?v=e0afb5d8:1676
    InnerModuleEvaluation self-hosted:2384
    InnerModuleEvaluation self-hosted:2384
    InnerModuleEvaluation self-hosted:2384
    evaluation self-hosted:2335

```
# Vite Typescript + Tailwind Starter

Simple, opinionated, and **production-ready** project template for Vite.

See [changelog](./CHANGES.md) for latest changes.

## Features

- Vue 3
- Vuex 4 store (fully typed)
- TypeScript
- Tailwind CSS w/ JIT compiler + following plugins preinstalled
  - `@tailwindcss/aspect-ratio`
  - `@tailwindcss/line-clamp`
  - `@tailwindcss/typography`
  - `@tailwindcss/forms`
- PostCSS 8 w/ `postcss-nesting` plugin
- Eslint
- Prettier
- Alias `@` to `<project_root>/src`
- Define `_APP_VERSION` from `package.json` version at build time
- Using new `script setup` syntax (see [Vue rfc #227](https://github.com/vuejs/rfcs/pull/227))
- Cypress.io e2e tests (configured similarly to `vue-cli`)
- GitHub workflows
  - Dependabot
  - Automated e2e tests
- GitLab CI
## Project setup and usage

Install dependencies:

```
yarn
```

Run development server:

```
yarn dev
```

Open Cypress test runner:

```
yarn test
```

Run Cypress tests in headless mode:

```
yarn test:ci
```

## Contributing

Contributions are welcome! Please follow the [code of conduct](https://www.contributor-covenant.org/version/2/0/code_of_conduct/) when interacting with others.

---

[Follow @uninen](https://twitter.com/uninen) on Twitter
