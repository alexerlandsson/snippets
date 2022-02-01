# Stylelint

Boilerplate for a `.stylelintrc.json` file used to lint _scss_.

You'll find more information about Prettier on https://stylelint.io.

## File

Create a file called `.stylelintrc.json` in the project root and copy the following code into it. This stylelint is based on `stylelint-config-standard-scss` and works in combination with prettier for linting _scss_.

```json
{
  "extends": ["stylelint-config-standard-scss", "stylelint-config-prettier-scss"],
  "rules": {
    "value-keyword-case": [
      "lower",
      {
        "camelCaseSvgKeywords": true
      }
    ],
    "color-function-notation": "legacy",
    "alpha-value-notation": "number"
  }
}
```

## Install dependencies

Run the folling command to install stylelint.

```bash
npm install --save-dev stylelint stylelint-config-standard-scss stylelint-config-prettier-scss
```

## Run the lint

Run the lint running the following command.

```bash
npx stylelint "**/*.scss"
```
