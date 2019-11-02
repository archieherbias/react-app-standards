# Setup and configure eslint

### Lint setup for React Web App

**Install dependencies first**

Here are recommended list for dev dependencies following airbnb lint standard configs:

```bash
"babel-eslint"
"eslint"
"eslint-config-airbnb"
"eslint-config-prettier"
"eslint-plugin-import"
"eslint-plugin-jest"
"eslint-plugin-jsx-a11y"
"eslint-plugin-prettier"
"eslint-plugin-react"
"eslint-plugin-react-hooks"
"prettier"
```

```bash
yarn add eslint eslint-config-airbnb eslint-config-prettier eslint-plugin-import eslint-plugin-jest eslint-plugin-jsx-a11y eslint-plugin-prettier eslint-plugin-react eslint-plugin-react-hooks prettier -D
```

Add an .eslintrc.json in your project and copy this content:

```bash
{
  "extends": ["airbnb", "prettier", "plugin:jest/recommended"],
  "plugins": ["prettier", "jest", "react-hooks"],
  "parser": "babel-eslint",
  "rules": {
    "no-underscore-dangle": [2, { "allowAfterThis": true }],
    "prettier/prettier": ["error"],
    "react/jsx-filename-extension": "off",
    "react/prefer-stateless-function": [2, { "ignorePureComponents": true }],
    "react/state-in-constructor": "off",
    "react-hooks/rules-of-hooks": "error", // Checks rules of Hooks
    "react-hooks/exhaustive-deps": "warn" // Checks effect dependencies
  },
  "globals": {
    "fetch": false,
    "window": true,
    "localStorage": true,
    "document": true,
    "IntersectionObserver": true
  },
  "settings": {
    "import/resolver": {
      "node": {
        "moduleDirectory": ["node_modules", "src"]
      }
    },
    "import/core-modules": [
    ]
  }
}
```

### Lint setup for React Native App

**Install dependencies first**

Here are recommended list for dev dependencies following react native community lint standard configs:

```bash
"@babel/core"
"@babel/runtime"
"@react-native-community/eslint-config"
"babel-jest"
"eslint"
"eslint-config-prettier"
"eslint-plugin-prettier"
"jest"
"metro-react-native-babel-preset"
"react-test-renderer"
```

Add an .eslintrc.json in your project and copy this content:

```bash
{
  "extends": ["@react-native-community", "prettier"],
  "plugins": ["prettier"],
  "parser": "babel-eslint",
  "rules": {
    "no-underscore-dangle": [2, { "allowAfterThis": true }],
    "prettier/prettier": [
      "error",
      { "singleQuote": true, "trailingComma": "all" }
    ],
    "react/jsx-filename-extension": "off",
    "react/prefer-stateless-function": [2, { "ignorePureComponents": true }],
    "react/state-in-constructor": "off"
  },
  "globals": {
    "fetch": false
  },
  "settings": {
    "import/resolver": {
      "node": {
        "moduleDirectory": ["node_modules", "app"]
      }
    },
    "import/core-modules": []
  }
}
```

### Lint setup for an expo app

**Install dependencies first**

_NOTE: This config can be used with bare react native project as well without the `babel-preset-expo`._

Here are recommended list for dev dependencies following airbnb lint standard configs:

```bash
"@babel/core"
"babel-eslint"
"babel-preset-expo"
"eslint"
"eslint-config-airbnb"
"eslint-config-prettier"
"eslint-plugin-import"
"eslint-plugin-jest"
"eslint-plugin-jsx-a11y"
"eslint-plugin-prettier"
"eslint-plugin-react"
"eslint-plugin-react-hooks"
"prettier"
```

Add an .eslintrc.json in your project and copy this content:

```bash
{
  "extends": ["airbnb", "prettier", "plugin:jest/recommended"],
  "plugins": ["prettier", "jest"],
  "parser": "babel-eslint",
  "rules": {
    "no-underscore-dangle": [2, { "allowAfterThis": true }],
    "prettier/prettier": ["error"],
    "react/jsx-filename-extension": "off",
    "react/prefer-stateless-function": [2, { "ignorePureComponents": true }],
    "react/state-in-constructor": "off",
    "react/jsx-props-no-spreading": "off"
  },
  "globals": {
    "fetch": false
  },
  "settings": {
    "import/resolver": {
      "node": {
        "moduleDirectory": ["node_modules", "src"]
      }
    },
    "import/core-modules": []
  }
}

```
