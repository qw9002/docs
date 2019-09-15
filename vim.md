vim 使用技巧
---

1. 普通模式
2. 插入模式
3. 可视模式

a. `g` `ctrl-a` 在可视模式下使用自增

> vip g<c-a>

test        1. test
test   =>   2. test
test        3. test

4. 命令模式


用 `ctrl-a` 使字母自增
`set nrformats+=alpha`

a => b

> 只能匹配一个模块

:{start},{end}

> 匹配多个模块

:g/{start} .,{finsh} norm
