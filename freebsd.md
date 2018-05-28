FreeBSD



https://download.freebsd.org/ftp/releases/VM-IMAGES/11.1-RELEASE/amd64/Latest/FreeBSD-11.1-RELEASE-amd64.vmdk.xz

![](/assets/FreeBSD_vm.png)

默认root无密码

修改root 密码 passwd 然后输入2次密码。

开启SSH

编辑/etc/inetd.conf，去掉ssh前的\#

编辑/etc/rc.conf，添加一行sshd\_enable="YES"

编辑/etc/ssh/sshd\_config，将

        \#PermitRootLogin no改为PermitRootLogin yes  //允许root登陆

        \#PasswordAuthentication no改为PasswordAuthentication yes//使用系统PAM认证

        \#PermitEmptyPasswords no改为PermitEmptyPasswords no//不允许空密码

保存退出

启动SSHD服务，/etc/rc.d/sshd start

查看服务是否启动，netstat -an，如果看到22端口有监听

adduser添加新用户

准备好你的账号和ssh客户端登录吧

