# Qt-Student-Information-Management-System
基于Qt界面的学生信息管理系统

本项目用的Qtcreater5.12 开发的 大家最好用Qtcreater 5.12以上 打开项目. 5.0版本以下可能会打不开项目 <br><br>

程序依赖于mysql数据库先要解决Qt连接数据库问题，大家出问题八成是连接数据库的配置没做。并且还有就是libmysql.dll文件的问题32位的Qt 对应32位的MySQL dll文件，同理64位对应64位不然会依然连接不上数据库！！！<br>
###一．使用说明<br>
该学生信息管理系统使用的数据库为MySQL；<br>
电脑运行时运行环境必须满足以下要求：<br><br>
1,电脑必须要安装数据库MySQL;安装引导里一定要将默认的latin1编码换成utf8编码，不然后面会中文乱码<br><br>
2,在电脑的MySQL中导入本人数据库脚本文件  studentmanager.sql  （该文件已打包好）<br><br>
3，在MySQL的安装目录下的lib文件夹中的libmysql.dll文件复制到Qt安装目录下的bin目录中<br><br>
4，最后在原代码中的globle.cpp 文件中更改连接数据库的账号和密码( 更改QString sqluser="root"  的值为更改账号。更改QString sqlpass="root" 的值为更改密码。<br><br>
此处我的数据库账号为root   密码为root。此处账号密码要对应自己MySQL账号密码）<br><br>
以上步骤若没完成则会编译运行不了<br><br>
学生端登录账密码在student表中可以找到 用该表的name作为账号， password 作为密码可登录学生端如：张三  123456<br><br>
管理员端登录账号密码在admin表中 用该表的username作为账号和password作为密码可登录管理员端 如admin  admin<br><br>
关于一些你们遇到的一些问题的总结：<br>
1.登陆显示密码错误，并且控制台打印not open database,这是链接数据库不成功，两个问题第一检测dll文件有没有导入，第二请使用我上面给的qtcreater,和mysql 安装包<br><br>
2.遇到信息显示中文乱码，请重新安装数据在数据库的安装引导中将默认的latin1编码换成utf8编码，然后确认在navacte 中你的数据库是不是设置为utf8编码,这两步缺一不可。<br>
