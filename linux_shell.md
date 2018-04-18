# Linux Shell

## .bashrc .bash_profile [参考](https://www.cnblogs.com/kevingrace/p/8072860.html)

- /etc/profile: 此文件为系统的每个用户设置环境信息,当用户第一次登录时,该文件被执行.并从/etc/profile.d目录的配置文件中搜集shell的设置.
- /etc/bashrc:  为每一个运行bash shell的用户执行此文件.当bash shell被打开时,该文件被读取.
- ~/.bash_profile: 每个用户都可使用该文件输入专用于自己使用的shell信息,当用户登录时,该文件仅仅执行一次!默认情况下,他设置一些环境变量,执行用户的.bashrc文件.
- ~/.bashrc: 该文件包含专用于你的bash shell的bash信息,当登录时以及每次打开新的shell时,该该文件被读取.
- ~/.bash_logout: 当每次退出系统(退出bash shell)时,执行该文件.

/etc/profile中设定的变量(全局)的可以作用于任何用户,而~/.bashrc等中设定的变量(局部)只能继承/etc/profile中的变量.

## add users

adduser:会自动为创建的用户指定主目录,系统shell版本,会在创建时输入用户密码.

useradd:需要使用参数选项指定上述基本设置,如果不使用任何参数,则创建的用户无密码,无主目录,没有指定shell版本.

## su

- su 不添加参数是切换到root用户
- su tom 切换到tom身份

## sudoers

- 第一种方法,修改`/etc/sudoers`文件. 切换至root身份, 文件添加写权限`chmod u+w /etc/sudoers`, 编辑此文件, 添加`username ALL=(ALL)ALL`, 撤销写权限`chmod u-w /etc/sudoers`.
- 第二种方法,`sudo usermod -a -G sudo username`

## add-apt-repository command not found

- sudo apt-get install python-software-properties
- sudo apt-get update
- sudo apt install software-properties-common 
- sudo apt-get update

## shells

`cat /etc/shells`

## ssh

`ssh username@address`
