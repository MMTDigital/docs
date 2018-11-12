# @mmtdigital/stylelint-config

---
#### ⚡️ Project Links ####
- **Repo**: https://github.com/MMTDigital/stylelint-config  
- **NPM Package**: https://www.npmjs.com/package/@mmtdigital/stylelint-config  
- **Current Version**:  [![NPM version][npm-image]][npm-url]
---

## Description
A standard set of rules for style linting at MMT Digital. To be used in conjunction with [stylelint](https://github.com/stylelint/stylelint).

The main reason you might want to use this package is to suggest a change to a linting rule. To do this, please submit a Github issue here: https://github.com/MMTDigital/stylelint-config/issues.

If you are developing a build package, or would like to genuinely use this package as a standalone linter config, carry on reading!

## Installation
```bash
npm i stylelint @mmtdigital/stylelint-config --save-dev
```

## Configuration
Include the following in your package.json
```json
  "stylelint": {
    "extends": "@mmtdigital/stylelint-config"
  }
```

To lint your code, either use the stylelint CLI or add stylelint to your editor (or do both). More here: https://stylelint.io/#getting-started

[npm-image]: https://img.shields.io/npm/v/@mmtdigital/stylelint-config.svg?style=flat-square
[npm-url]: https://www.npmjs.com/package/@mmtdigital/stylelint-config
