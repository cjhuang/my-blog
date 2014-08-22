# Linux
-----------

> Something about Linux and Free Software

-----------

# Something

## How to adjust the bright throught command
we can use the following command to adjust the brightness
> echo 120 | sudo tee /sys/class/backlight/intel_backlight/brightness
>> note: 120 is the brightness what we want. We can't throught edit the file
>> " /sys/class/backlight/intel_backlight/brightness "
>> directly to adjust the brightness.

If when the system is turned on, the brightness is our hope, we should add
the line "echo 120 | sudo tee
/sys/class/backlight/intel_backlight/brightness" to /etc/rc.local befor the
line "exit 0" in that file. The conent of
/sys/class/backlight/intel_backlight/max_brightness is the maximum
brightness of PC.

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
  + Perl
+ Terminal
  + [rxvt or rxvt-unicode (urxvt)](http://rxvt.sourceforge.net/ "rxvt")
  + xterm
+ Window Manager
  + [FVWM](http://www.fvwm.org/ "FVWM")
  + [Sawfish](http://xwinman.org/sawfish.php "Sawfish")
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
