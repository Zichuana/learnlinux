# Linux Note

### 删除用户

管理员权限下（`su/sudo`）

方法一：

1. 使用`userdel text`删除用户账号
2. 使用`rm -r/-rf /home/text `删除用户家文件
3. 使用`rm /var/spool/mail/text`删除用户邮件信箱

方法二：

​	`userdel -r text`删除用户

### wt操作虚拟机

1. 使用命令`ifconfig`或者`ip addr`查看用户ip

2. 在wt输入命令`ssh XXX@ip`

3. `exit`退出登入

### 配置ssh

1. `nuname`获取设备名称`master`
2. `cd /root`根目录
3. `ssh-keygen -t rsa`紧跟三次回车，生成无密码密钥对
4. `ssh-copy-id  master`生成公钥验证文件
5. `ssh master`验证密钥是否完成

### Ubuntu打开虚拟机后经行的操作

- 构建虚拟机时断网

`sudo apt update`更新软件源

`sudo apt install open-vm-tools`全屏

`sudo apt upgrade`更新软件

### Ubuntu下vi编辑器问题

默认情况下ubuntu上也安装有vi但是奇怪的是这个vi是vim-common版本，基本上用不了所以要先把这个版本的vi卸载掉才可以，卸载命令是：

`sudo apt-get remove vim-common`

卸载成功之后接着执行 :

`sudo apt-get install vim`

### Ubuntu下安装gcc出现错误：无法修正错误，因为您要求某些……

是Ubuntu自生安装的软件版本高，而所安装软件的依赖包版本低的原因

`sudo apt-get install aptitude`

`sudo aptitude install g++`

选择降级
