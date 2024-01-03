# react-monorepo-starter-ts
- quickstart monorepo example for js/ts/react projects
# overview
- tech-stack
  - typescript v5
  - npm workspaces
  - rspack
    - rspack config shared at top level with webpack-merge
    - hot reloading ready
  - jest for testing
  - styling: support scss/css
  - other devtools: eslint, prettier

- project-structure
  - packages
    - foo: utils
    - bar: depends on foo
  - apps
    - app-nodejs: simple nodejs utils
    - app-react-rspack: simple react app
# quickstart
- requirements
  - npm v7+

```shell
# build all packages
npm run build

# start demo app
cd apps/app-react-rspack
npm i
npm start
```

- open a browser and go to http://localhost:8999
# usage
- `APP_ENV` environment variable
  - if no value is set, building es6 and ts is supported, but not react
  - if `react*` is set, building react is supported
  - if `reacthot` is set, react hot reloading is supported
# notes/limitations
- npm
  - `npm run build` has to run twice because npm workspaces doesn't support pkg compiled by dependent order
# roadmap
- rspack
  - esm-output is only supported in canary channel
  - HMR is not implemented for module chunk format yet
# license

[MIT](https://opensource.org/licenses/MIT)
