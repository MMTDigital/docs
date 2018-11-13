# @mmtdigital/mmt-webpack

---
#### ⚡️ Project Links ####
- **Repo**: https://github.com/MMTDigital/mmt-webpack  
- **NPM Package**: https://www.npmjs.com/package/@mmtdigital/mmt-webpack  
- **Current Version**:  [![NPM version][npm-image]][npm-url]
---

## Description
`mmt-webpack` is a webpack setup that should handle most things you can chuck at it (within the MMT ecosystem, at least)! It's capable of handling all the latest JavaScript, React, styles, filetypes. But the true beauty of using this package is that fact that we can upgrade our webpack setup on multiple projects over time.

For example, if a new version of webpack gets released — we can upgrade and test this package and consumers (MMT projects) can choose to upgrade by bumping their version in the project's `package.json`. We will use semver versioning to ensure that if there are breaking changes, you will be aware of it.

Another huge benefit is that if you happen to find a bug in the webpack setup (very likely), we can patch the bug and **all other projects benefit**!

## Getting started
**If you have generated your project with `generate-project`, this package will already be setup for you.** 

If you would like to consume this package manually, or migrate an old project across, here are the steps:

```bash
npm i @mmtdigital/mmt-webpack --save-dev
```

Then add this to your npm scripts in your `package.json`:

```json
"npm start": "mmt-webpack --dev"
```

## Configuration
You must provide a config. The config file is called `mmt.config.js` and should be placed in a `config` directory in the root of your project.

```
- config
  - mmt.config.js
```

Here is an example `mmt.config.js` file:

```js
module.exports = {
  entry: './src/index.js'
}
```

The only requirement is an entry point. However, there are other options available:

#### **entry** _{string} | required_
The file that webpack should use as an entry point 

#### **output** _{string} | default: `'./build'`_
Where you would like to output your files, relative to the project

#### **verbose** _{boolean} | default: `false`_
Show more verbose webpack logging. Warning, this is messy (but useful for errors)

#### **imageDataUri** _{boolean} | default: `false`_
Convert all images under 8kb to data URIs. This is only of use in full React projects, not Kentico projects.

#### **postCssEnvOptions** _{object} | default: See below_
Passes a configuration object for PostCSS env. See more here: https://preset-env.cssdb.org. The default options are:

```js
{
  stage: 0,
  browsers: [
    'last 2 versions',
    'IE >= 9',
    'safari >= 8'
  ]
}
```

## Usage
This project will provide you with two available tasks.

#### Development builds (automatically watches files)

```bash
mmt-webpack --dev
```

- This build automatically watches files. To disable this pass the flag `--no-watch`
- The files will be fully expanded and have source maps, for easier debugging

#### Production builds

```bash
mmt-webpack
```

- This build will be heavily compressed an minified
- The process will exit as soon as the bundle is built
- `console.log` statements and code comments will be removed

## Extending Webpack
The webpack setup is actually extendable. Please consider if what you're extending would be better to be worked back into the base package for others to use. If not, here is how to extend:

Create a file called `extends.js` in the `config` directory at the root of your project.

```
- config
  - mmt.config.js
  - extends.js
```

The file should be setup like this:
```js
exports.webpackDev = {}

exports.webpackProd = {}
```

As you can probably see, you have control to extend either the `development` or `production` builds. Any config you provide here will be deeply merged into the webpack config before execution. You config must be a valid webpack config. You can read more about webpack configs here: https://webpack.js.org/configuration

Unfortunately, a caveat to this approach is that a lot of webpack plugins require webpack as a dependency. Even though `mmt-webpack` has this dependency, your project will require it too. We haven't found a work-around to this, so our recommendation is to try and work your feature back into the package. We can always make it configurable :)

TODO: Add linting docs

[npm-image]: https://img.shields.io/npm/v/@mmtdigital/mmt-webpack.svg?style=flat-square
[npm-url]: https://www.npmjs.com/package/@mmtdigital/mmt-webpack
