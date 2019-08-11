# `@ronanc/prettier-config`

My personal Prettier configuration.

## Usage

In order to use this package:

- Install the package:
  > This will install the package, and add it to the `devDependencies` list in your `package.json` file:

```sh
$ npm install --save-dev @ronanc/prettier-config
```

**package.json**:

```jsonc
{
  // ...
  "devDependencies": {
    "@ronanc/prettier-config": "0.1.0"
  }
}
```

- Change your prettier configuration file name to: `.prettierrc.js`.
  > It needs to be a JS file so you can use `modules.exports`.
- Require this package in the `.prettierrc.js` file:
  > Use the JS spread operator to pull all of the properties out of the required package JSON file.

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
