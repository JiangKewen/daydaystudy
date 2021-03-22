# jkw

## eslint+prettier

1. npm install --save-dev eslint prettier eslint-config-prettier eslint-plugin-prettier
2. vscode 安装相关插件
3. .prettierrc
```json
{
  "singleQuote": true,
  "semi": false,
  "trailingComma":"all",
  "arrowParens":"always",
  "printWidth": 120
}
```
4. .eslintrc
```json
{
  "env": {
    "browser": true,
    "node": true,
    "es6": true
  },
  "parserOptions": {
    "parser": "babel-eslint",
    "sourceType": "module"
  },
  "extends": ["prettier"],
  "plugins": ["prettier"],
  "rules": {
    "prettier/prettier": "error",
    "prefer-arrow-callback": "off",
    "semi": [2, "never"]
  }
}
```
