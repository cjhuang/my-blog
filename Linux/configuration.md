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
