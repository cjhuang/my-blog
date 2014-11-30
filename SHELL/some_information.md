# some information #

## which ##
使用which寻找命令所根据的路径是由PATH变量定义的，故不同的用户
使用which命令所得结果可能不同,加上-a选项则列出所有可以找到的同
名执行文件，否则纸列出第一个

## whereis ##
查找特定文件

## locate ##
查找任意文件，不过是利用数据库(位置：/var/lib/mlocate/)来查找，
速度比find快，但查询到的
不一定是最新结果，除非数据库刚进行了更新。这里就涉及到如何手动
进行数据库的更新(不同的distribution自动更新数据库的时间不同)。
守栋更新数据库可以使用updatedb，这个命令会去读取/etc/updatedb.conf
这个配置文件的设置

## find ##
find是一个非常强大的查找命令，下面列出几个用法
### 根据文件时间查找： find [PATH] [option] [action] ####
在文件属性里关于时间的有mtime(内容)，ctime(状态)，atime(读取)。下面
仅就mtime为例。

> -mtime  n: n为数字，n天之前的一天之内
>
> -mtime +n: n天之前(不含n天本身)被更改多的文件名
>
> -mtime -n: n天之内(含n天本身)
>
> -newer file: file为一个存在的文件，列出比file还要新的文件名

### 与用户或用户组有关的参数 ###

## iconv ##
语系编码转换命令
--list : 列出iconv支持的语系数据

iconv -f 原本编码 -t 新编码 filename [-o newfile]
最后一个选项的作用是保留原本的文件

例：将big5编码的文件file.big5转换成utf8编码的文件file.utf8
iconv -f big5 -t utf8 file.big5 -o file.utf8
