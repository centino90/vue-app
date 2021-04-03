# vue-app

testing a new vue app with vue-cli, vue router, vuex, vuetify

# Setting up

## Project setup

```
npm install
```

## Compiles and hot-reloads for development

```
npm run serve
```

## Compiles and minifies for production

```
npm run build
```

## Lints and fixes files

```
npm run lint
```

## Customize configuration

See [Configuration Reference](https://cli.vuejs.org/config/).

## Edit .eslint.js file

```javascript
module.exports = {
  root: true,
  env: {
    node: true,
  },
  extends: ["plugin:vue/essential", "plugin:prettier/recommended", "eslint:recommended", "@vue/prettier"],
  parserOptions: {
    parser: "babel-eslint",
  },
  rules: {
    "no-console": process.env.NODE_ENV === "production" ? "warn" : "off",
    "no-debugger": process.env.NODE_ENV === "production" ? "warn" : "off",
  },
};
```

## Create .prettierrc.js file and add these configurations

```javascript
module.exports = {
  singleQuote: false,
  semi: false,
};
```

## configure user preferences settings and add

```javascript
"vetur.validation.template": false,
"eslint.validate": [
        {
            "language": "vue",
            "autoFix": true
        },
        {
            "language": "html",
            "autoFix": true
        },
        {
            "language": "javascript",
            "autoFix": true
        }
    ],
  "eslint.autoFixOnSave": true,
  "editor.formatOnSave": true,
```
