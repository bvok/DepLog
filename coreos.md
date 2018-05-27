# 1.CoreOS

下载

[https://stable.release.core-os.net/amd64-usr/current/coreos\_production\_vmware\_image.vmdk.bz2](https://stable.release.core-os.net/amd64-usr/current/coreos_production_vmware_image.vmdk.bz2)

注意一定是vmdk格式，用来制作腾讯云镜像。

修改密码

1.启动CoreOS,运行到grub界面时，赶紧按下"E"键，进入编辑模式

2.添加coreos.autologin到如下位置即可

3.输入完成后按"F10"重启

4.进入到shell界面后，即可使用passwd core命令修改密码

