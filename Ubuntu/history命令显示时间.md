#  Ubuntu 中执行history命令显示时间：

介绍四种方式：

**1. 修改/etc/profile，在最后添加下面一行**

`export HISTTIMEFORMAT="%F %T `whoami` "`

退出用户，重新登录后生效

缺点：只有用户加载其用户环境后才能生效。比方说从普通用户切换到root，如果只执行

sudo su是不能生效的，只有执行了sudo su - 加载了root用户环境后执行history命令才能生效

**2. 修改用户的.profile文件**

`vim ~/.profile`

在最后添加下面一行

`export HISTTIMEFORMAT="%F %T `whoami` "`

缺点：跟上面1一样，并且这个只对设置了的用户，执行history命令时才生效。

**3. 修改/etc/bash.bashrc文件，在最后添加下面一行**

`export HISTTIMEFORMAT="%Y-%m-%d %H:%M:%S "`

无需加载用户环境变量，在任何用下执行history时候都可以生效。缺点，记录中不显示哪个用户执行了某个命令。

**4. 修改用户.bashrc文件**

`vim ~/.bashrc`

在最后添加下面一行

`export HISTTIMEFORMAT="%F %T `whoami` "`

只对设置了的用户，执行history命令时才生效。缺点，记录中不显示哪个用户执行了某个命令。



