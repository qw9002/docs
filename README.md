todo list
---------

<!-- vim-markdown-toc GFM -->

* [语言](#语言)
    * [nodejs](#nodejs)
        * [nodejs 库](#nodejs-库)
        * [`typescript` 的使用](#typescript-的使用)
    * [vim 使用技巧](#vim-使用技巧)
        * [snippet 学习使用](#snippet-学习使用)
        * [脚本学习](#脚本学习)
    * [Linux](#linux)
* [书籍](#书籍)
    * [你所不知道的 `javascript` 的学习](#你所不知道的-javascript-的学习)
    * [深入理解计算机系统](#深入理解计算机系统)

<!-- vim-markdown-toc -->

# 语言

## nodejs

- [ ] js单线程，Node多线程执行
- [ ] 事件循环介绍
- [ ] Promise在事件循环哪个环节
- [ ] process.nextTick setImmediate 区别, 各自嵌套会有什么后果
- [ ] Express 转 Koa, 切换原因，Express中间件转Koa中间件怎么替代
- [ ] Koa 的 洋葱模型, 中间件怎么串起来的，next 代表了什么了, 有没了解过内部的 koa-compose是怎么执行的
- [ ] require cache, import区别
- [ ] 多进程怎么弄，cluster，node是怎么实现的，node的
- [ ] node 中的内存泄漏
- [ ] 有没有用过egg
- [ ] 闭包定义
- [ ] Object.create 原型链
- [ ] Es6
- [ ] 跟Es5比起来主要的几个特性
- [ ] 类的构造函数的 super
- [ ] 箭头函数解决了什么问题
- [ ] Promise, 看过实现没
- [ ] 有几个方法
- [ ] 有几种状态
- [ ] then的第二个函数的.catch的区别
- [ ] Typescript
- [ ] TS JS 区别
- [ ] ES5 转 TS 过程
- [ ] declare 关键字
- [ ] .d.ts文件作用
- [ ] 命名空间的作用和模块
- [ ] Nginx


### nodejs 库

- [ ] koa
- [ ] sequelize
- [ ] egg


### `typescript` 的使用

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


[文件地址](./typescript.md)


## vim 使用技巧

[vim](./vim/README.md)

[tips](./vim/skills.md)

### snippet 学习使用

### 脚本学习


## Linux

- [ ] 用什么系统
- [ ] 文件权限, 664，chmod
- [ ] 文件归属 chown
- [ ] 打包 压缩呢
- [ ] 查看磁盘，查看内存
- [ ] 查看代码文件，倒叙呢
- [ ] kill 和 kill -9 的区别
- [ ] 定时任务呢
- [ ] proc目录


# 书籍

## 你所不知道的 `javascript` 的学习


## 深入理解计算机系统

```
2~3章：
汇编语言 王爽（三） (pdf)
加密解密 (pdf)

4~6章：
计算机系统要素 (pdf)
计算机组成结构：硬件/软件接口 (书籍)
7~8章：
程序员的自我修养 (pdf/书籍)

9~12章：
现代操作系统 (书籍)
unix 环境高级编程 (书籍/pdf 英语)
网络编程 (书籍)
```
