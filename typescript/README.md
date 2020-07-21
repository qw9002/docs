typescript
------------

<!-- vim-markdown-toc GFM -->

* [typescript 使用 eslint](#typescript-使用-eslint)
* [项目创建](#项目创建)
* [export、import、export default 区别](#exportimportexport-default-区别)

<!-- vim-markdown-toc -->

## typescript 使用 eslint

由于 tslint 项目不在维护 [tslint 不在维护](https://eslint.org/blog/2019/01/future-typescript-eslint#linting)
`typescript` 使用 `eslint` 语法检测。

## 项目创建

1. 创建项目目录: mkdir project && cd project
2. 通过 `yarn init` 或 `npm init` 初始化, 生成 `package.json` 文件,
3. 添加语法检测库及局和模块类型定义包

[为什么使用这三个包](https://github.com/typescript-eslint/typescript-eslint#how-do-i-configure-my-project-to-use-typescript-eslint)

```bash
yarn add --registry=https://registry.npm.taobao.org --dev @typescript-eslint/parser
yarn add --registry=https://registry.npm.taobao.org --dev @typescript-eslint/eslint-plugin
yarn add --registry=https://registry.npm.taobao.org --dev @typescript-eslint/typescript-estree

yarn add --registry=https://registry.npm.taobao.org --dev @types/node # 支持nodejs全局和模块类型定义
```

4. 配置 .eslintrc.js 文件

在项目目录下创建 `.eslintrc.js` 文件, 支持语法检测

```javascript

module.exports = {
  // 支持 typscript 语法检测
  parser: '@typescript-eslint/parser',
  extends: 'eslint-config-alloy',
  // 添加规则
  plugins: [
    '@typescript-eslint'
    // 'typescript'
  ],
  // 运行环境
  env: {
    browser: true, // 浏览器
    node: true,
    es6: true
  },
  globals: {
    Atomics: 'readonly',
    SharedArrayBuffer: 'readonly'
  },
  parserOptions: {
    ecmaVersion: 2017, // ECMA 2017 标准
    sourceType: 'module', // module 模式
    ecmaFeatures: { jsx: true }
  },
  // off: 0, warn: 1, error: 2
  rules: {
    semi: 2,
    eqeqeq: [
      2, 'always', { null: 'ignore' }
    ],
    'no-undef': 2,
    'no-unused-vars': 1
  },
  overrides: [
    {
      files: ['*.ts', '*.tsx'],
      rules: {
        // 修复 ts 的问题：使用接口类型，但报未使用错误
        '@typescript-eslint/no-unused-vars': [
          2, { args: 'none' }
        ]
      }
    }
  ]
};

```

## export、import、export default 区别

[import](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Statements/import)

