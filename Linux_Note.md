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
