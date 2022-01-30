# Stylelint

Boilerplate for a `.prettierrc.json` file used to format primarily _scss_. This requires prettier to be install in your code editor.

You'll find more information about Prettier on https://prettier.io.

## File

Create a file called `.prettierrc.json` in the project root and copy the following code into it. These local rules will overwrite global settings for the specific project.

```json
{
  "printWidth": 100,
  "tabWidth": 2,
  "singleQuote": false,
  "trailingComma": "es5",
  "endOfLine": "lf",
  "useTabs": false
}
```

## Install dependencies

Run the folling command to install prettier.

```bash
npm install --save-dev --save-exact prettier
```

## Run the lint

Run prettier by running the following command.

```bash
npx prettier --write .
```
