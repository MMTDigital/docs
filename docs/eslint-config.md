# @mmtdigital/eslint-config

---
#### ⚡️ Project Links ####
- **Repo**: https://github.com/MMTDigital/eslint-config  
- **NPM Package**: https://www.npmjs.com/package/@mmtdigital/eslint-config  
- **Current Version**:  [![NPM version][npm-image]][npm-url]
---

## Description
A standard set of rules for JavaScript linting at MMT Digital. To be used in conjunction with [ESLint](https://eslint.org/).

The main reason you might want to use this package is to suggest a change to a linting rule. To do this, please submit a Github issue here: https://github.com/MMTDigital/eslint-config/issues.

**If your project uses the `@mmtdigital/webpack` package, you do not need to install this manually!**

If you are developing a build package, or would like to genuinely use this package as a standalone linter config, carry on reading!

## Installation
```bash
npm i eslint eslint-plugin-import eslint-plugin-node eslint-plugin-promise eslint-plugin-standard babel-eslint @mmtdigital/eslint-config --save-dev
```

## Usage
Either, add to your package.json:

```json
"eslintConfig": {
    "extends": "@mmtdigital/eslint-config",
}
```

Or, configure webpack to deal with it:

```bash
npm i eslint-loader --save-dev
```

```js
{
  test: /\.(js|jsx|mjs)$/,
  exclude: /node_modules/,
  rules: [
    {
      enforce: 'pre',
      loader: require.resolve('eslint-loader'),
      options: {
        emitError: true,
        configFile: require.resolve('@mmtdigital/eslint-config')
      }
    }
  ]
}
```



[npm-image]: https://img.shields.io/npm/v/@mmtdigital/eslint-config.svg?style=flat-square
[npm-url]: https://www.npmjs.com/package/@mmtdigital/eslint-config
