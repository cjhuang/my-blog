# Linux
-----------

> Something about Linux and Free Software

-----------

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


# Something others

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

## How to link to wireless network ##
无线网卡配置

此页由Linux Wiki用户Chenxing于2008年11月27日 (星期四) 09:28的最后更改。
在1233456的工作基础上。
本文介绍在Linux命令行界面中手动配置无线网卡的方法。目前流行的多数发行版都支持用图形界面的network-manager方便地进行配置，而无需使用本文所介绍的原始方法。下面介绍使用iwconfig和ifconfig等命令在命令行状态下配置无线网络。前题是无线网卡驱动已经正确安装，并被系统正确识别。

工作的大体思路如下：

用iwconfig开启无线网卡的电源，并查找区域内的无线网络
连接到相应的无线网络
通过ifconfig启用无线网卡，并获取IP（如果使用DHCP的话）
注意：
假设无线被识别为wlan0，如果您的网卡没有被识别为wlan0，可以在操作时做相应的修改。
具体过程
1. 打开无线网卡电源

iwconfig wlan0 txpower on

2. 列出区域内的无线网络

iwlist wlan0 scan

3. 假设要连接到网络MyHome（即essid为MyHome的网络），那么输入命令

iwconfig wlan0 essid "MyHome"

如果网络是加密的，密码是0123456789，那么就输入命令

iwconfig wlan0 essid "MyHome" key 0123-4567-89

4. 如果正常的话，输入

iwconfig wlan0

就可以看到连接正常的各项参数了。 5. 启用无线网卡

ifconfig wlan0 up

6. 如果是用DHCP获取IP的，那么用dhclient或dhcpcd获取ip

dhclient wlan0
或
dhcpcd wlan0

7. 现在无线网卡应该可以正常使用了

# How to open doc, xls, ppt file using wps
doc: wps file.doc

xls: et  file.xls

ppt: wpp file.ppt
> use touch file.doc/xls, we can bulid a file doc or xls,
> but not for ppt. We can use '>file.doc/xls' to build file.

# How to update softeware and system
sudo apt-get update
sudo update-manager -d

# How to inhibite Linux to visit certain website
edit the file "/etc/hosts", add follow
127.0.0.1  the.name.of.website
