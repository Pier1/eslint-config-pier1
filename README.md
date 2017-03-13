# eslint-config-pier1

[![Build Status](https://travis-ci.org/pier1/eslint-config-pier1.svg?branch=master)](https://travis-ci.org/pier1/eslint-config-pier1)
[![npm version](https://img.shields.io/npm/v/bootstrap.svg)](https://www.npmjs.com/package/eslint-config-pier1)
[![devDependencies Status](https://david-dm.org/ariyalabs/eslint-plugin-demandware/dev-status.svg)](https://david-dm.org/pier1/eslint-config-pier1?type=dev)

> ESLint [shareable config](http://eslint.org/docs/developer-guide/shareable-configs.html)


## Installation

```
$ npm install --save-dev eslint babel-eslint eslint-config-pier1
```


## Usage

Once the [`eslint-config-pier1`](http://github.com/Pier1/eslint-config-pier1) package is installed, you can use it by specifying `pier1` in the [`extends`](http://eslint.org/docs/user-guide/configuring#extending-configuration-files) section of your [ESLint configuration](http://eslint.org/docs/user-guide/configuring).

```js
{
  "extends": "pier1",
  "rules": {
    // Additional, per-project rules...
  },
  "globals": {
    // Additional, per-project `no-undef` ignores...
  }
}
```

### Using the `pier1` config with `eslint:recommended`

There are several rules in the [`eslint:recommended` ruleset](http://eslint.org/docs/rules/) that you might want to override and enforce in your project.

To use Pier 1 Imports style in conjunction with ESLint's recommended rule set, extend them both, making sure to list `pier1` last:

```js
{
  "extends": ["eslint:recommended", "pier1"],
  "rules": {
    // Additional, per-project rules...
  },
  "globals": {
    // Additional, per-project `no-undef` ignores...
  }
}
```

To see how the `pier1` config compares with `eslint:recommended`, refer to the [source code of `index.js`](https://github.com/pier1/eslint-config-pier1/blob/master/index.js), which lists every ESLint rule along with whether (and how) it is enforced by the `pier1` config.

### Using the `pier1` config with [`eslint-plugin-demandware`](http://github.com/ariyalabs/eslint-plugin-demandware)

Demandware has numerous globals that need to be defined so that ESLint will not warn about their usage.

Once the [`eslint-plugin-demandware`](http://github.com/ariyalabs/eslint-plugin-demandware) package is installed, you can use it by specifying `demandware` in the [`plugins`](http://eslint.org/docs/user-guide/configuring#configuring-plugins) and `demandware/globals` in the [`env`](http://eslint.org/docs/user-guide/configuring#specifying-environments) section of your [ESLint configuration](http://eslint.org/docs/user-guide/configuring).

```js
{
  "extends": ["eslint:recommended"], "pier1",
  "rules": {
    // Additional, per-project rules...
  },
  "plugins": [
    // Additional, per-project plugins...
    "demandware"
  ],
  "env": {
    // Additional, per-project environments...
    "demandware/globals": true
  },
  "globals": {
    // Additional, per-project `no-undef` ignores...
  }
}
```

## License

Licensed under the [MIT License](LICENSE).

Copyright (c) 2017 Pier 1 Imports, Inc.
