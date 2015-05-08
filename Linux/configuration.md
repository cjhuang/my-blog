# 一些有用的设置 #

## 关于Linux的字体 ##
+ 安装字体   将字体文件(*.ttc)文件从windows或者网上下载
下来，然后在/usr/share/fonts中创建一个文件夹，例如msfonts，
将字体文件拷贝到该文件夹内，进入该文件夹，依次执行如下命令：

> sudo mkfontdir
>
> sudo mkfontscale
>
> sudo fc-cache

到此字体便安装完成了。

+ 在Ubuntu上安装新的字体后浏览器或者其他一些软件在显示
中文时字体会发生变化，这是由于在文件/etc/fonts/conf.d/65-nonlatin.conf中
定义了选用字体的先后顺序，此时只需将该文件中你想要的字体
挪到前面即可，有三处需要改动。

> 参考文章: [Ubuntu 13.10 中文字体设置](http://www.cnblogs.com/daizhe11/p/3384391.html)

## 设置文件的默认打开方式
文件默认打开方式的设置存储在/usr/share/applications/default.list(全局文件关联)和~/.local/share/applications/mimeapps.list(个人文件关联)中，我们只需要修改后者即可。打开那个文件就知道怎么修改了。该文件中的那些*.desktop文件存储在/usr/share/applications/文件夹中，可根据需要模仿已有的desktop文件编辑自己的desktop文件。xdg-open即是根据我们的设置来打开文件的。

## 建立wifi热点 ##
安装ap-hotspot
$ sudo add-apt-repository ppa:nilarimogard/webupd8
$ sudo apt-get update
$ sudo apt-get install ap-hotspot

然后配置wifi热点
$ sudo ap-hotspot configure
注意：设置的密码不能太短，太短则无法建立，具体要多长不清楚

然后启动
$ sudo ap-hotspot start
若显示Another process is already running
则
$ sudo rm /tmp/hotspot.pid
Bug:
若运行 sudo ap-hotspot start 后一直ting留在Starting Wireless Hotspot...
则是hostapd的问题，新版本有问题，要退回到老版本，卸载这个软件后
wget http://old-releases.ubuntu.com/ubuntu/pool/universe/w/wpa/hostapd_1.0-3ubuntu2.1_i386.deb
sudo dpkg -i hostapd*.deb
sudo apt-mark hold hostapd (防止hostapd又更新到新版本)

