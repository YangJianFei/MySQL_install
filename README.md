# MySQL_install
install MySQL all Step(Personal)

1.下载MySQL安装包。
2.安装。--默认目录为：C:\Program Files\MySQL\MySQL-版本.
3.以管理员方式进入命令行进入安装bin目录。--命令:cd C:\Program Files\MySQL\MySQL-版本\bin
4.输入命令:mysqld install
5.命令:mysqld --initialize-insecure
6.net start mysql
7.mysql -u root -p 键入密码   查看原始随机密码地址C:\Program Files\MySQL\MySQL Server 5.7\data\XXX.err
8.修改密码 mysql> ALTER USER 'root'@'localhost' IDENTIFIED BY '你的密码';
9.配置环境变量
虽然打开mysql 了，但每次打开mysql 都要输入那么多指令切换目录是不是很讨厌？怎么弄呢？

右键我的电脑->属性->高级系统设置->环境变量->path->编辑，将你的mysql软件下的bin目录的全路径放里面。最后在那个目录的路径后面加个英文的分号（;）保存就行了。如D:\mysql\mysql-x.x.xx-winx64\bin;

为啥这样弄呢？简单的说环境变量里面的path路径，就是cmd系统的查找目录路径。你输入一个指令，系统怎么知道这个指令有没有呢？系统做了什么事？其实系统是在当前目录和系统环境变量path里面的路径全部查找一边，找到第一个为准，找不到就报错。所以我们要不每次都切换cmd目录，要不就设置了，以后就不需要再切换cmd路径了。

打个比方：系统就像一辆公交车，按着既定的路线走，环境变量里面的路径就是那个路线或者说是各个站，到了站（找到第一个）就下车。
http://www.jb51.net/article/83643.htm
