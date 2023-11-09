# prettier-config

> Shareable Prettier config for my projects to produce neat and readable code

## Highlights

- Prints **single quotes instead of double quotes** (_including inside of JSX_)
- Prints **trailing commas where possible** (_excluding function parameters and calls_)
- Prints **single attribute per line** in HTML, Vue and JSX
- **Removes semicolons at the ends of statements**

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
  "prettier": "@s1mpson/prettier-config"
}
```

- Or by creating `.prettierrc` or `.prettierrc.json` file with the name of this package as its only content:

```jsonc
"@s1mpson/prettier-config"
```

Voilà! You now have a working Prettier configuration!
