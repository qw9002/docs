vim
---

1. 普通模式
2. 插入模式
3. 可视模式
4. 命令模式

1 g-ctrl-a 在普通模式下使用自增

> vip g<c-a>

> 0. test        1. test
> 0. test   =>   2. test
> 0. test        3. test

使字母自增

`set nrformats+=alpha`

> 使用<c-a>自增字母

a => b

> 只能匹配一个模块

:{start},{end}

> 匹配多个模块

:g/{start} .,{finsh} norm
