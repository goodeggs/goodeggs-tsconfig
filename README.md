# @goodeggs/tsconfig

Shared TypeScript configuration files for use in Good Eggs modules and applications.

## Installation

Install via npm:

```sh
$ npm install --save-dev @goodeggs/tsconfig
```

Install via yarn:

```sh
$ yarn add --dev @goodeggs/tsconfig
```

## Usage

> NOTE: These configurations are intended for use with Babel. If you are transpiling via `tsc`, these configurations will not work for you!

Use the [`extends` property](https://www.typescriptlang.org/docs/handbook/tsconfig-json.html#configuration-inheritance-with-extends) in your `tsconfig.json` to inherit from these shared configurations:

```json
{
  "extends": "@goodeggs/tsconfig/base"
}
```

## Releasing

This repo is **not** currently configured to publish automatically from CI.

To release a new version of this module, use yarn locally to publish the version and create the git tag, then push:
```sh
yarn publish --new-version=<major|minor|patch>
git push --follow-tags
```

### Listing of Configurations

- `@goodeggs/tsconfig/base`: A base configuration. Makes no assumptions about the environment you're targeting.
- `@goodeggs/tsconfig/browser`: A base browser configuration. Assumes you are targeting an ESNext feature set (and using Babel to achieve compatibility with older browsers if desired).
- `@goodeggs/tsconfig/react`: A React/JSX configuration. Assumes you are targeting an ESNext feature set (and using Babel to achieve compatibility with older browsers if desired).
