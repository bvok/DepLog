pkg install postgresql10-server-10.3\_1

echo "postgresql\_enable=\"YES\"" &gt;&gt; /etc/rc.conf

~~chown pgsql:pgsql /root/pgsql~~

/usr/local/etc/rc.d/postgresql initdb

/usr/local/etc/rc.d/postgresql start

pw usershow -a

su postgres

~~psql -U pgsql postgres~~

alter user postgres with password ‘pwd’

## 信任远程连接 {#信任远程连接}

查找 find . -name pg\_hba.conf

编辑 pg\_hba.conf

host    all             all             0.0.0.0/0               trust

编辑 postgresql.conf

监听 listen\_addresses = '\*'

端口 port=5432



