# **_package.json_** boilerplate

This is a customized `package.json` boilerplate tailored for JavaScript projects using webpack, eslint, prettier, cypress, and more. It provides a well-structured foundation, saving you time on configuring essential tools and dependencies.

[![license](https://img.shields.io/badge/License-MIT-blue.svg?style=flat)](LICENSE)

## Features

- Pre-configured `package.json` optimized for JavaScript projects.
- Includes configurations for Webpack, ESlint, Prettier, Cypress, and more.
- Designed to streamline the setup process for your projects.
- Open-source and available for everyone to use and customize.

## Usage

1. Download the [`package.json`](package.json) file from this repository.
2. Customize the downloaded `package.json` file to match your project's requirements.
3. Use it as a starting point for your JavaScript projects with ease.

If you find this boilerplate helpful, don't forget to give it a star!

```
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
  "keywords": [
    "package.json",
    "boilerplate"
  ],
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
      "path": "./node_modules/cz-conventional-changelog",
      "disableScopeLowerCase": true
    }
  }
}
```

## Contributing

Want to contribute? All contributions are welcome. Read the [contributing guide](CONTRIBUTING.md).

## Questions

If you have questions tweet me at [@sandro_m_m](https://twitter.com/sandro_m_m) or [open an issue](../../issues/new).

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details

**~ sharing is caring ~**
