# Eslint, Prettier, Editor-config and Create-react-app.

(2020/07)

## Starting the project:

### With NPM, NPX and YARN:

```jsx
npm init react-app my-app
npx create-react-app my-app
yarn create react-app my-app
```

## Add the following developer dependencies:

- eslint-config-airbnb
- eslint-plugin-import
- eslint-plugin-jsx-a11y
- eslint-plugin-react

```powershell
yarn add eslint-config-airbnb eslint-plugin-import eslint-plugin-jsx-a11y eslint-plugin-react -D
```

## Add ESLint and Prettier to the VSCode extensions:

![Eslint Extension](https://github.com/oscarel/config-style-guides/blob/master/images_readme/ESLint-extencion.png?raw=true)

![Prettier Extension](https://github.com/oscarel/config-style-guides/blob/master/images_readme/Prettier-extencion.png?raw=true)

## Create a document at the root of your project called ".eslintrc".

```json
.eslintrc
```

## Edit the .eslintrc.json created. Place:

```json
{
  "parser": "babel-eslint",
  "env": {
    "browser": true,
    "jest": true
  },
  "plugins": ["import", "jsx-a11y", "react"],
  "extends": "airbnb",
  "rules": {
    "react/jsx-filename-extension": [
      "error",
      {
        "extensions": [".js", ".jsx"]
      }
    ],
    "global-require": "off",
    "import/prefer-default-export": "off",
    "no-unused-expressions": ["error", { "allowTaggedTemplates": true }],
    "linebreak-style": "off",
    "react/state-in-constructor": "off",
    "react/static-property-placement": "off",
    "react/jsx-one-expression-per-line": "off"
  }
}
```

## How to interact with Prettier with ESLint:

### First you must open your VSCode settings (Ctrl + Shift + p) (JSON). Right after, you must add the following command:

```json
"editor.codeActionsOnSave": {
    // For ESLint
    "source.fixAll.eslint": true,
    // For TSLint
    "source.fixAll.tslint": true,
    // For Stylelint
    "source.fixAll.stylelint": true
}
```

### * My default settings:

```json
{
  "workbench.colorTheme": "Dracula",
  "workbench.iconTheme": "material-icon-theme",
  "terminal.integrated.shell.windows": "C:\\Program Files\\Git\\bin\\bash.exe",
  "editor.codeActionsOnSave": {
    // For ESLint
    "source.fixAll.eslint": true,
    // For TSLint
    "source.fixAll.tslint": true,
    // For Stylelint
    "source.fixAll.stylelint": true
  },
  "editor.fontFamily": "Fira Code",
  "editor.fontLigatures": true,
  "editor.rulers": [80, 120],
  "editor.renderLineHighlight": "gutter",
  "editor.tabSize": 2,
  "terminal.integrated.fontSize": 14,
  "emmet.includeLanguages": {
    "javascript": "javascriptreact"
  },
  "emmet.syntaxProfiles": {
    "javascript": "jsx"
  },
  "javascript.updateImportsOnFileMove.enabled": "never",
  "editor.parameterHints.enabled": false,
  "breadcrumbs.enabled": true,
  "javascript.suggest.autoImports": false,
  "[javascript]": {
    "editor.defaultFormatter": "HookyQR.beautify"
  }
}
```

## Add the editorconfig extension to VSCode:

![Editorconfig extension](https://github.com/oscarel/config-style-guides/blob/master/images_readme/editorconfig.png?raw=true)

## Create an editorconfig document at the root of your project:

![Editorconfig generate](https://github.com/oscarel/config-style-guides/blob/master/images_readme/editorconfigcreate.png?raw=true)

## Configure the created document. Replace with:

```jsx
root = true

[*]
indent_style = space
indent_size = 2
charset = utf-8
trim_trailing_whitespace = true
insert_final_newline = true
```

## 🎉🎉 Configuration completed successfully! 🎉🎉
