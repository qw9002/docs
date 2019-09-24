> 删除可执行文件
> 因为 find 不能通过 -type 选项来确认可执行文件
find . -perm 755 -a -type f -exec rm {} \;

# vim

## 修改

> 小修改

修改 -> .(repeat 重复)

> 批量修改

录制宏 -> 修改 -> @req -> @@

> 全局替换

:%s/partern/replece/g

> 所有文件的替换

:argdo %s/partern/replece/g
