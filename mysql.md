#### ERROR 1819 (HY000): Your password does not satisfy the current policy requirements
```
$ sudo mysql -u root -p
  show variables like 'validate_password%';
  SET GLOBAL validate_password.special_char_count = 0;
  ALTER USER 'root'@'localhost' IDENTIFIED BY 'password';u
  FLUSH PRIVILEGES;
  exit

```
#### MySQL Error: : 'Access denied for user 'root'@'localhost'
```
$ sudo mysql -u root -p
  ALTER USER 'root'@'localhost' IDENTIFIED BY 'erebor';
  FLUSH PRIVILEGES;
  exit
$ mysql -u root -p
```


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
