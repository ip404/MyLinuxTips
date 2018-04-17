# Linux Shell

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

## pip3

- sudo apt-get install python3-pip
