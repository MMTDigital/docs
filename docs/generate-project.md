# @mmtdigital/generate-project

---
#### ⚡️ Project Links ####
- **Repo**: https://github.com/MMTDigital/generate-project   
- **NPM Package**: https://www.npmjs.com/package/@mmtdigital/generate-project    
- **Current Version**:  [![NPM version][npm-image]][npm-url]
---

# Quick Start

1. The best way to use this tool is by using `npx`. So, first up, make sure you're on the [latest stable version of node and npm](node-and-npm.md). This is really important.

2. Navigate to a directory that you would like a project to be set up and run:

```
npx @mmtdigital/mmt
```

That's it! You will be prompted for the rest of the setup.

## I'm struggling to use npx...
If you're truly struggling to upgrade npm and node and cannot use `npx` — please reach out on the `#front-end` Slack channel. However — there is always the option to install the package globally and run it:

```
npm i -g @mmtdigital/mmt
```
```
mmt
```

**This is not recommended. Please don't do this.**


## What is this?

**In simple terms, this is `create-react-app` for MMT projects**

`@mmtdigital/mmt` is a command line tool can help greatly in setting up front-end projects. In fact, it's the recommended way to get started with a new project. We are hoping for this tool to grow multiple uses. Currently, this tool will scaffold you a front-end project with:

✅ A recommended folder structure  
✅ A fully ES6+ build setup  
✅ `dev` and `prod` builds  
✅ Style and JS linting  
✅ Pre-commit hooks  
✅ A full testing set up  

# Rationale – Advantages

* Simple set up of new sites (perfect for the lead dev on the project)
* _Upgradable_ build set up! As Webpack and Babel upgrade — so can your project
* Fixing your build bugs fixes everyone's build bugs
* Encourages a more open source model

## Separation of concerns

One of the most exciting things about this setup is that it's all completely separate npm packages. Meaning that your setup will actually consist of:

* https://github.com/MMTDigital/mmt-webpack
* https://github.com/MMTDigital/stylelint-config
* https://github.com/MMTDigital/eslint-config

So, your webpack setup is completely controlled by the npm package version you specify.


[npm-image]: https://img.shields.io/npm/v/@mmtdigital/stylelint-config.svg?style=flat-square
[npm-url]: https://www.npmjs.com/package/@mmtdigital/stylelint-config
