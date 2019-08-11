# Prettier Configuration

My personal Prettier configuration.

## Usage

In order to use this package:

- Add this package (`@ronanc/prettier-config`) to your `package.json` file.
- Change your prettier configuration file name to: `.prettierrc.js`.
- Require this package.

## Overriding style rules

You can override style rules like so:
**.prettierrc.js**:

```ts
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
