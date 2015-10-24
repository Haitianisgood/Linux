#  ubuntu 中 update与upgrade的作用及区别
在Ubuntu下有一个软件源列表，源列表里面都是一些网址信息，这每一条网址就是一个源，这个地址指向远程源服务器上有哪些软件可以安装使用。

## 源列表文件：

/etc/apt/sources.list       系统默认的源列表文件

/etc/apt/sources.list.d     用户自定义的源列表文件

在源列表文件中，添加源，只需要按照源的格式填写就好，不需要只需要在指定源前面加入 # 符号就可以了

自定义的源列表文件，需要以“.list”结尾

## update：

执行：

`$sudo apt-get update 或是 # apt-get update`

这个命令，会访问源列表里的每个网址，并读取软件列表，然后保存在本地电脑。在软件包管理器里看到的软件列表，都是通过update命令更新的。

## upgrade:

执行：

`$sudo apt-get upgrade或#apt-get upgrade`

upgrade 是升级已安装的所有软件包，升级之后的版本就是本地索引里的，因此，在执行 upgrade 之前一定要执行 update, 这样才能是最新的。

upgrade升级软件包，其实也会包括内核文件。所请尽量不要轻易执行apt-get upgrade

## 参考网址

[Ubuntu_软件包管理](http://wiki.ubuntu.com.cn/UbuntuManual:Ubuntu_软件包管理#.E8.AE.BE.E7.BD.AE_APT)

