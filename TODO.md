# Node

- js单线程，Node多线程执行
- 事件循环介绍
- Promise在事件循环哪个环节
- process.nextTick setImmediate 区别, 各自嵌套会有什么后果
- Express 转 Koa, 切换原因，Express中间件转Koa中间件怎么替代
- Koa 的 洋葱模型, 中间件怎么串起来的，next 代表了什么了, 有没了解过内部的 koa-compose是怎么执行的
- require cache, import区别
- 多进程怎么弄，cluster，node是怎么实现的，node的
- node 中的内存泄漏
- 有没有用过egg

# Javescript

- 闭包定义
- Object.create 原型链
- Es6
- 跟Es5比起来主要的几个特性
- 类的构造函数的 super
- 箭头函数解决了什么问题
- Promise, 看过实现没
- 有几个方法
- 有几种状态
- then的第二个函数的.catch的区别
- Typescript
- TS JS 区别
- ES5 转 TS 过程
- declare 关键字
- .d.ts文件作用
- 命名空间的作用和模块
- Nginx


# TCP/IP
- 三次握手四次挥手
- TIME-WAIT, 主动方收到 FIN, 返回收到对方 FIN 的 ACK, 等待对方是否真的收到了 ACK, 如果过一会又来一个 FIN, 表示对方没收到, 这时要再 ACK 一次
# HTTP
# HTTP2
# HTTPS
# 机制怎么回事
# 分布式
# Mysql
# Mongo
# Redis

# 比较Mysql, Mongo, Redis

- 平时怎么用的，sequelize
- 事务解决了什么问题
- group查询
- 子查询
- 用过哪些
- Docker
- Go
- 切片, len, cap, append 元素，超过 cap 会怎样
- new 和 make 的区别，map、slice 和channel, make(chan int, 2)
- Shell
- Express 转 Koa
- 其他
- 前端了解程度
- 跟前端打交道程度
- 其他方面的知识
- graphql
- webpack的架构，插件机制，插件是怎么做的
- http2 的几个特点，原理
- babel做了什么事情
- cdn 的实现原理
- 单点登录的实现
- oauth2的实现
- 缓存穿透, 缓存血崩

## 记录一下前端面试题

1. 浏览器本地存储？
2. web storage和cookie的区别
3. 请描述一下 cookies、 sessionStorage和localstorage区别？
4. 常见的HTTP状态码？（后面ajax请求会写到）
5. bootstrap响应式实现的原理?
6. Vue请求数据的方式
7. 如何优化页面，加快页面的加载速度（面五次有一次问到的概率）
8. 评测你写的前端代码性能和效率？（问到一次）
9. iframe的优缺点？（问到一次） 
10. Http与Https的区别
11. vuex的属性
12. vue双向绑定的原理
13. h
14. vue全家桶
15. MVVM思想:Vue.js是一套构建用户界面的MVVM框架
16. 合并数组
17. 垂直居中的方式flex + justify-content + align-items.parent {
display: flex;
justify-content: center; //水平居中
align-items: center; //垂直居中
}
18. call,apply,bind的区别？
19. 为什么使用axios？
20. new操作的过程？
21. vuex原理？
22. vue怎么实现页面的权限控制？
23. 真实DOM和虚拟DOM的区别？
24. 怎么解决跨域（概率 90%，此问题想到一位奇葩的面试官，记忆犹新！）
25. 请简述JavaScript中的this？
26. JS哪些操作会造成内存泄露？
27. 如何确定this指向？
28. 箭头函数和普通函数有什么区别？
29. 怎么理解闭包？
30. 如何实现原型继承？
31. 讲讲输入完网址按下回车，到看到网页这个过程中发生了什么？
32. 谈谈你对前端性能优化的理解？
33. es 6 新语法？
34. Promise 对象？
35. 请你谈谈Cookie的弊端？
36. 对BFC规范的理解？
38. 你常使用的库有哪些？常用的前端开发工具？开发过什么应用或组件？
39. 列举IE与其他浏览器不一样的特性？
40. 什么叫优雅降级和渐进增强？
41. WEB应用从服务器主动推送Data到客户端有那些方式？
42. 请解释一下 JavaScript 的同源策略？
43. ajax的步骤？
44. 一次js请求一般情况下有哪些地方会有缓存处理？
45. 一个页面上有大量的图片，加载很慢，你有哪些方法优化这些图片的加载？
46. .谈谈以前端角度出发做好SEO需要考虑什么？
47. get、 post的区别？
48. var a;        console.log(a) 求结果？原因？
49. transform和transition的区别？
50. mounted中常用的方法？
51. 钩子函数（问了无数次）？
52. 清除浮动的方法？(多次出现在面试题)
53. position有哪些属性？
54. 隐藏一个div有几种方法？
55. 登陆注册怎么做？
56. 计算属性和监听器有什么区别？computed、watch
57. v-for渲染列表是key是用来做什么的？       为了高效的更新虚拟DOM
58. 数据请求在生命周期哪一个阶段？
59. 给DOM元素绑定事件有哪些方法？
60. 数组里面有哪些遍历方法？es6 for(){} 遍历forEach 遍历for-in 遍历for-of 遍历every()、some()、filter()、map()、reduce（）、reduceRight()
61. 用js可以实现的动画  为什么要用css？       css渲染的动画不占用js主线程
62. ajax请求数据重新处理和拦截器？
