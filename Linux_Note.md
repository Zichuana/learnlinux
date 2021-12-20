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
