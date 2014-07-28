# Software list
-----------

## Contain
+ Program
  + Vim
  + Shell
  + Fortran
  + Lisp ( Scheme )
  + Python
  + Java
+ Office
  + Xpad
+ Entertainment
  + NetHack
  + VLC

-------------
### Program
-------------

### Vim
### Shell
### Fortran
### Lisp ( Scheme )
### Python
### Java

-------------
### Office
-------------

### Xpad
Xpad是一款非常小巧的记事本或者说是便签，相当实用。可以通过
在终端运行 sudo apt-get install xpad 进行安装。它可以提供
很多个便签，每个便签是相互独立的。界面如下

![xpad1](https://github.com/cjhuang/my-blog/blob/master/Picture/xpad1.png)

当有多个便签时如果是通过图形界面点击启动 Xpad 或者是在终端
输入 xpad & 启动的话将只会启动一个便签，那其它便签怎么启
动呢？这个看一下 Xpad 的 man 手册就可以，使用 -s 参数
便是启动所有的便签。

若你嫌每次开机都要手动启动 Xpad 麻烦的话，你可以在你的当前
用户目录下找有没有如下三个文件

> ~/.bash_profile
>
> ~/.bash_login
>
> ~/.profile
>

在任意一个文件的最末行后新加一行，写上上 xpad -s & 便可以
了，这样每次开机后就会显示所有便签。

> 注：一定记得写 &, 否则计算机就停在这个命令上了，此时你就
> 需要去控制台修改你改动的那个文件并重启

-------------
### Entertainment
-------------

### [NetHack](http://www.nethack.org/)
### VLC
