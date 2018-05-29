pkg install postgresql10-server-10.3\_1

echo "postgresql\_enable=\"YES\"" &gt;&gt; /etc/rc.conf

~~chown pgsql:pgsql /root/pgsql~~

/usr/local/etc/rc.d/postgresql initdb

/usr/local/etc/rc.d/postgresql start

psql -U pgsql postgres

alter user postgres with password ‘pwd’

