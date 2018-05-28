# FreeBSD

## 下载

[https://download.freebsd.org/ftp/releases/VM-IMAGES/11.1-RELEASE/amd64/Latest/FreeBSD-11.1-RELEASE-amd64.vmdk.xz](https://download.freebsd.org/ftp/releases/VM-IMAGES/11.1-RELEASE/amd64/Latest/FreeBSD-11.1-RELEASE-amd64.vmdk.xz)

下载Virtual Machine Images架构amd64

![](/assets/FreeBSD_vm.png)

# 配置

### 改密码

默认root无密码

修改root 密码 passwd 然后输入2次密码。

### 开启SSH

编辑/etc/inetd.conf，去掉ssh前的\#

编辑/etc/rc.conf，添加一行sshd\_enable="YES"

编辑/etc/ssh/sshd\_config，将

```
    #PermitRootLogin no改为PermitRootLogin yes  //允许root登陆 ，可添加新账户绕开此配置

    #PasswordAuthentication no改为PasswordAuthentication yes//使用系统PAM认证

    #PermitEmptyPasswords no改为PermitEmptyPasswords no//不允许空密码
```

保存退出

启动SSHD服务，/etc/rc.d/sshd start

查看服务是否启动，netstat -an，如果看到22端口有监听

### 添加新用户

adduser

su命令的用户必须属于wheel组\(root的基本属组，组ID为0\),编辑组设置文件/etc/group，将需要超级用户权力的管理成员加入到wheel组中。

vi /etc/group

wheel:\*:0:root,core

准备好你的账号和ssh客户端登录吧

### 镜像制作

镜像制作其他类似腾讯云

