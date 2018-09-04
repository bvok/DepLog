ln
``` sh
ln -s /home/user/sys/usr/local/code/bin/code code
ln -s /home/user/sys/usr/local/flutter/bin/flutter flutter
ln -s /home/user/sys/usr/local/go/bin/go go
ln -s /home/user/sys/usr/local/go/bin/godoc godoc
ln -s /home/user/sys/usr/local/go/bin/gofmt gofmt
ln -s /home/user/sys/usr/local/idea/bin/idea.sh idea
ln -s /home/user/sys/usr/local/jdk/bin/java java
ln -s /home/user/sys/usr/local/jdk/bin/javac javac
ln -s /home/user/sys/usr/local/jdk/bin/jar jar
ln -s /home/user/sys/usr/local/julia/bin/julia julia
ln -s /home/user/sys/usr/local/liteide/bin/liteide liteide
```
env
```sh
export GTK_IM_MODULE=fcitx
export XMODIFIERS=@im=fcitx
export QT_IM_MODULE=fcitx
export JAVA_HOME=/home/user/sys/usr/local/jdk/
export GOROOT=/home/user/sys/usr/local/go/
export PATH="$PATH:/home/user/sys/bin/"
export PUB_HOSTED_URL="https://pub.flutter-io.cn"
export FLUTTER_STORAGE_BASE_URL="https://storage.flutter-io.cn"
```
vnc
``` sh
#!/bin/sh
# Uncomment the following two lines for normal desktop:
unset SESSION_MANAGER
unset DBUS_SESSION_BUS_ADDRESS
#exec /etc/X11/xinit/xinitrc
[ -x /etc/vnc/xstartup ] && exec /etc/vnc/xstartup
[ -r $HOME/.Xresources ] && xrdb $HOME/.Xresources
xsetroot -solid grey
vncconfig -iconic &
#xterm -geometry 80x24+10+10 -ls -title "$VNCDESKTOP Desktop"&
#twm &
startxfce4 &
```
