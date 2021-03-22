# jkw

## eslint+prettier

1. npm install --save-dev eslint prettier eslint-config-prettier eslint-plugin-prettier
2. npm i -d eslint @typescript-eslint/parser @typescript-eslint/eslint-plugin
3. npm i -g prettier eslint-config-prettier eslint-plugin-prettier
4. vscode 安装相关插件
5. .prettierrc
```json
{
  "singleQuote": true,
  "semi": false,
  "trailingComma": "all",
  "arrowParens": "always",
  "printWidth": 120,
  "bracketSpacing": false,
  "jsxBracketSameLine": true,
  "insertPragma": true,
  "tabWidth": 4,
  "useTabs": false  
}
```
6. .eslintrc
```json
{
  "env": {
    "browser": true,
    "node": true,
    "es6": true
  },
  "parserOptions": {
    "parser":  "@typescript-eslint/parser", //定义ESLint的解析器
    "sourceType": "module",
    "ecmaVersion": 2019
  },
  "extends": ["prettier", "plugin:@typescript-eslint/recommended", "prettier/@typescript-eslint",
    "plugin:prettier/recommended"],
  "plugins": ["prettier", "@typescript-eslint"],
  "rules": {
    "prettier/prettier": "error",
    "prefer-arrow-callback": "off",
    "semi": [2, "never"]
  }
}
```
7. [参考](https://segmentfault.com/a/1190000019661168)
