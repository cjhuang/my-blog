#  Fortran 编程中遇到的Bug
---------

> 第一大原则：**能简单就简单，最好不用写注释就可以看懂**
> 
> 书写规范
> 
> * 程序开头说明程序作用，并列数据字典
> * 大写Fortran保留字和常量，变量名、过程名等用小写
> * 记得在主程序、子程序、模块和函数中加 "*IMPLICIT NONE*" 语句
> * 变量使用前记得初始化
> * 记得回显输入程序的数据
> * 尽量使用整型指数，用实型指数计算速度慢而且精度低
> * 用圆括号使赋值语句功能更清晰
> * 输出数据最好带单位

## Bug ##

* 在shell中当用重定向符 "<" 为程序提供数据时，程序中所有从外部
  读取数据的操作将都从用重定向符定向的文件中读取数据

