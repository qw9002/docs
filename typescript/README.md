typescript
------------

<!-- vim-markdown-toc GFM -->

* [`typescript` 的使用](#typescript-的使用)

<!-- vim-markdown-toc -->

## `typescript` 的使用

> 由于 tslint 项目不在维护 [tslint 不在维护](https://eslint.org/blog/2019/01/future-typescript-eslint#linting)
`typescript` 使用 `eslint` 语法检测。

1. 在项目目录下创建 `package.json` 文件, 通过 `yarn init` or `npm init`

```bash
yarn add --registry=https://registry.npm.taobao.org --dev @typescript-eslint/parser @typescript-eslint/eslint-plugin @typescript-eslint/typescript-estree
```

[为什么使用这三个包](https://github.com/typescript-eslint/typescript-eslint#how-do-i-configure-my-project-to-use-typescript-eslint)

2. 配置 `.eslintrc.js` 文件

在项目目录下创建 `.eslintrc.js` 文件

```javascript

module.exports = {
  // 支持 typscript 语法检测
  parser: '@typescript-eslint/parser',
  // 添加规则
  plugins: [
    // 'typescript',
  ],
  // 运行环境
  env: {
    browser: true,
    node: true,
    es6: true,
  },
  globals: {
    Atomics: 'readonly',
    SharedArrayBuffer: 'readonly',
  },
  parserOptions: {
    ecmaVersion: 2017,
    sourceType: 'module',
    ecmaFeatures: {
      jsx: true,
    },
  },
  rules: {
    semi: 'error',
    eqeqeq: ['error', 'always', { null: 'ignore', }],
    'no-undef': 'error',
    'no-unused-vars': 1,
    'typescript/no-unused-vars': 1,
    'typescript/class-name-casing': 'error',
  },
  overrides: [
    {
      files: ['*.ts', '*.tsx'],
      rules: {
        // 修复 ts 的问题：使用接口类型，但报未使用错误
        '@typescript-eslint/no-unused-vars': [2, { args: 'none' }],
      }
    }
  ]
};

```

3. export、import、export default

[import](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Statements/import)

