#### Reset Mysql Password

```
$ sudo mysql_secure_installation
```
or

```
$ sudo /etc/init.d/mysql stop
$ sudo mysqld --skip-grant-tables &
$ mysql -u root mysql
UPDATE mysql.user SET Password = PASSWORD('enter password')
WHERE User = 'root';
FLUSH PRIVILEGES;
exit;
```
