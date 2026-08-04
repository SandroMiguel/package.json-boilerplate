# **_package.json_** boilerplate

This is my personal `package.json` boilerplate for JavaScript projects using Webpack, ESLint, Prettier, Cypress, Jest, Storybook and other common tools. Feel free to use it as a starting point or as inspiration for your own projects.

[![license](https://img.shields.io/badge/License-MIT-blue.svg?style=flat)](LICENSE)

## Features

- Pre-configured `package.json` optimized for JavaScript projects.
- Includes common scripts for Webpack, ESLint, Prettier, Cypress, Jest, Storybook, and more.
- Designed to streamline the setup process for your projects.
- Open source and available for everyone to use and customize.

## Usage

Download the latest `package.json`:

```bash
curl -o package.json https://raw.githubusercontent.com/SandroMiguel/package.json-boilerplate/master/package.json
```

Or simply copy and paste the contents of [`package.json`](package.json) into your project.

Then customize it to match your project's requirements.

If you find this boilerplate helpful, don't forget to give it a star!

## Example

Below is a simplified example of the boilerplate:

```json
{
  "name": "package.json-boilerplate",
  "version": "1.0.0",
  "description": "The inspirational package.json boilerplate",
  "main": "index.js",
  "license": "MIT",
  "author": {
    "name": "Sandro Miguel Marques",
    "email": "sandromiguel@sandromiguel.com",
    "url": "http://sandromiguel.com"
  },
  "keywords": ["package.json", "boilerplate"],
  "repository": {
    "type": "git",
    "url": "https://github.com/SandroMiguel/package.json-boilerplate.git"
  },
  "bugs": {
    "url": "https://github.com/SandroMiguel/package.json-boilerplate/issues"
  },
  "scripts": {
    "start": "webpack --mode development --watch --progress",
    "lint": "eslint src --ext js",
    "lint:fix": "eslint src --ext js --fix",
    "format": "prettier --write 'src/**/*.{js,json,css}'",
    "format:php": "prettier",
    "stylelint": "stylelint './src/**/*.{css,scss}'",
    "stylelint:fix": "stylelint './src/**/*.{css,scss}' --fix",
    "test": "jest",
    "test:watch": "jest --watch",
    "test:phpunit": "./vendor/bin/phpunit --colors=always",
    "e2e": "cypress open",
    "increment-build": "node buildIncrementer.js",
    "build": "yarn increment-build && webpack --mode production --progress",
    "release": "git pull && yarn build && git add . && git commit -m 'build to production' --no-verify && git push",
    "sync:cecilia-css": "rsync -r -t --progress --delete ../cecilia-css/ ./node_modules/cecilia-css/",
    "sync:ubiquitous-components": "rsync -r -t --progress --delete ../ubiquitous-components/lib/ ./node_modules/ubiquitous-components/lib/ && yarn start",
    "sync:verum-php": "rsync -r -t --progress --delete ../verum-php/src/ ./vendor/sandromiguel/verum-php/src/",
    "upgrade-deps": "yarn upgrade-interactive --latest",
    "storybook": "storybook dev -p 6006",
    "build-storybook": "storybook build"
  },
  "config": {
    "commitizen": {
      "path": "cz-conventional-changelog",
      "disableScopeLowerCase": true
    }
  },
  "devDependencies": {
    "cz-conventional-changelog": "^3.3.0"
  }
}
```

## Contributing

Want to contribute? All contributions are welcome. Read the [contributing guide](CONTRIBUTING.md).

## Questions

If you have questions, reach out on Twitter at [@sandro_m_m](https://twitter.com/sandro_m_m) or [open an issue](../../issues/new).

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

**~ sharing is caring ~**
