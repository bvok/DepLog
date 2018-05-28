# 1.CoreOS

## 下载CoreOS镜像

[https://stable.release.core-os.net/amd64-usr/current/coreos\_production\_vmware.vmx](https://stable.release.core-os.net/amd64-usr/current/coreos_production_vmware.vmx) 打开虚拟机需要

[https://stable.release.core-os.net/amd64-usr/current/coreos\_production\_vmware\_image.vmdk.bz2](https://stable.release.core-os.net/amd64-usr/current/coreos_production_vmware_image.vmdk.bz2) 镜像文件，需要解压缩

注意一定是vmdk格式，用来制作腾讯云镜像。

## 配置参数

通过VM加载系统vmx

VMWare出现文件未能锁定\(Failed to lock the file\)的解决方法

删除虚拟机配置文件和虚拟磁盘文件夹的所有以.lck结尾的文件以及文件夹

调整系统镜像配置参数，例如1C2G。

## 修改密码

1.启动CoreOS,运行到grub界面时，赶紧按下"E"键，进入编辑模式

2.添加coreos.autologin到如下位置即可

![](/assets/import.png)

3.输入完成后按"F10"重启

4.进入到shell界面后，即可使用sudo passwd core命令修改密码

## 上传镜像

通过腾讯云经对象存储上传虚拟机镜像文件。

![](/assets/CoreOS_vm_upload.png)

