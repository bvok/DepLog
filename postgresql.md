chown pgsql:pgsql /root/pgsql

/usr/local/etc/rc.d/postgresql initdb

/usr/local/etc/rc.d/postgresql start

psql -U pgsql postgres

alter user postgres with password ‘pwd’

