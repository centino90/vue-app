# vue-app
testing a new vue app with vue-cli, vue router, vuex, vuetify

# Setting up

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
    semi: false
}
```


