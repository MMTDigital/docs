# @mmtdigital/generate-project

---
#### ⚡️ Project Links ####
- **Repo**: https://github.com/MMTDigital/generate-project   
- **NPM Package**: https://www.npmjs.com/package/@mmtdigital/generate-project    
- **Current Version**:  [![NPM version][npm-image]][npm-url]
---

# Description
This package will boilerplate out a new project for you. This is the recommended approach to starting a new MMT Digital project

---
# Quick Start

- Get the latest stable Node.
- Navigate to a directory that you would like a project to be set up and run:

```bash
npx @mmtdigital/generate-project
```

That's it! You will be prompted for the rest of the setup.

---

## I'm struggling to use npx...
The best way to use this tool is by using `npx`. So, first up, make sure you're on the [latest stable version of node and npm](node-and-npm.md). This is really important.

If you're truly struggling to upgrade npm and node and cannot use `npx` — please reach out on the `#front-end` Slack channel. However — there is always the option to install the package globally and run it:

```bash
npm i -g @mmtdigital/generate-project
```

You will then be able to run it globally with the following command

```bash
generate-project
```

**This is not recommended. Please don't do this.**


## What is this?

**In simple terms, this is `create-react-app` for MMT projects**

`@mmtdigital/generate-project` is a command line tool can help greatly in setting up front-end projects. In fact, it's the recommended way to get started with a new project. We are hoping for this tool to grow multiple uses. Currently, this tool will scaffold you a front-end project with:

✅ A recommended folder structure  
✅ A fully ES6+ build setup  
✅ `dev` and `prod` builds  
✅ Style and JS linting  
✅ Pre-commit hooks  
✅ A full testing set up  

## Advantages

🎉  Simple set up of new sites (perfect for the lead dev on the project)  
🎉  Fully upgradable build set up! As Webpack and Babel upgrade — so can your project  
🎉  Fixing your build bugs fixes everyone's build bugs  
🎉  Encourages a more open source model  

## Separation of concerns

One of the most exciting things about this setup is that it's all completely separate npm packages. Meaning that your setup will actually consist of:

* https://github.com/MMTDigital/mmt-webpack
* https://github.com/MMTDigital/stylelint-config
* https://github.com/MMTDigital/eslint-config

So, your webpack setup is completely controlled by the npm package version you specify.

## Versioning against @mmtdigital/mmt-webpack

Everybody likes new and exciting tech to play with! So, when creating a project with `generate-project` we've ensured that you be able to have all the latest updates and fixes we'll be constantly applying to `@mmtdigital/mmt-webpack. 

Fear not! We'll be sticking to NPM's docs about semantic versioning, so any breaking changing will not be automatically included into your project and be issued as a new major version for your to upgrade when suitable. 

Including a reference like `"@mmtdigital/mmt-webpack": "^0.1.0"` in your package.json will allow your project to receive

✅ Patches/bug fixes  
✅ New non breaking features  

❌ New breaking changes

[NPM - About semantic versioning](https://docs.npmjs.com/about-semantic-versioning)

[npm-image]: https://img.shields.io/npm/v/@mmtdigital/generate-project.svg?style=flat-square
[npm-url]: https://www.npmjs.com/package/@mmtdigital/generate-project
