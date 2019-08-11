# `@ronanc/prettier-config`

My personal Prettier configuration.

## Usage

In order to use this package:

- Install the package:

```sh
$ npm install --save-dev @ronanc/prettier-config
```

- This will install the package, and add it to the `devDependencies` list in your `package.json` file:

```jsonc
{
  "devDependencies": {
    "@ronanc/prettier-config": "0.1.0"
  }
}
```

- Change your prettier configuration file name to: `.prettierrc.js`.
- Require this package in the `.prettierrc.js` file:

```js
module.exports = {
  ...require('@ronanc/prettier-config'),
};
```

## Overriding style rules

You can override style rules like so:
**.prettierrc.js**:

```js
module.exports = {
  ...require('@ronanc/prettier-config'),
  trailingComma: 'none',
  overrides: [
    {
      files: '*.html',
      options: {
        lineLength: 140,
      },
    },
  ],
};
```

## More information

For more information check out the Prettier site:  
https://prettier.io

Here's the section on having a shared config repository:  
https://prettier.io/docs/en/configuration.html#sharing-configurations
