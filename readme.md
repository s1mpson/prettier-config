# prettier-config

[![npm (scoped)](https://img.shields.io/npm/v/%40s1mpson/prettier-config)](https://www.npmjs.com/package/@s1mpson/prettier-config)
[![install size](https://packagephobia.com/badge?p=@s1mpson/prettier-config)](https://packagephobia.com/result?p=@s1mpson/prettier-config)
[![code style: prettier](https://img.shields.io/badge/code_style-prettier-ff69b4.svg)](https://github.com/prettier/prettier)

> Shareable Prettier config for my projects to produce neat and readable code

## Highlights

- Prints double quotes instead of single quotes (_including inside of JSX_) — MUCH less character escaping
- Prints trailing commas where possible (_excluding function parameters and calls_)
- Prints single attribute per line in HTML, Vue and JSX
- Adds semicolons at the ends of statements — _This proved to be a great visual cue_

## Install

First, you want to install this package as a dev dependency:

```bash
$ npm install -D @s1mpson/prettier-config
# or
$ yarn add -D @s1mpson/prettier-config
# or
$ pnpm add -D @s1mpson/prettier-config
# or
$ bun add -D @s1mpson/prettier-config
```

## Usage

Now, you just need to reference this module as your Prettier configuration.

- You can do it by either adding `"prettier"` key in your `package.json`:

```jsonc
{
  // ...
  "prettier": "@s1mpson/prettier-config",
}
```

- Or by creating `.prettierrc` or `.prettierrc.json` file with the name of this package as its only content:

```jsonc
"@s1mpson/prettier-config"
```

- Or by creating `prettier.config.js` file to be able to override any of the Prettier properties. For JSDoc type safety to work, you need to install "prettier" as a **dev** dependency via `npm install -D prettier`:

```js
import baseConfig from "@s1mpson/prettier-config";

/**
 * @type {import("prettier").Config}
 */
const config = {
  ...baseConfig,
  // Override any of the Prettier properties here:
  // singleQuote: false,
};

// If you rock ESM modules ("type": "module" in your package.json):
export default config;
// Or, if you're using CommonJS:
// module.exports = config
```

Voilà! You now have a working Prettier configuration!
