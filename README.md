# Database-Command-CLI
Command Line Databse

```    
mysql -u root -p
show databases;
CREATE DATABASE database_name CHARACTER SET utf8 COLLATE utf8_general_ci;
drop database database_name;
use IST_DB;
show tables;
describe table_name;
```
MySql Restart/Stop/Start:
----------------------------
```
sudo systemctl status mysqld.service
sudo systemctl start mysqld.service
sudo systemctl stop mysqld.service
```
Mysql DB Type:
-------------------
```
show table status;
```
Change utf:
--------------
```
ALTER DATABASE IST_DB CHARACTER SET utf8 COLLATE utf8_general_ci;
```
Change root pass:
-----------------------
```
ALTER USER 'root'@'localhost' IDENTIFIED BY 'MyNewPass';
```
Create New User:
-----------------
```
CREATE USER 'NewUser'@'localhost' IDENTIFIED BY 'new_password';
GRANT ALL PRIVILEGES ON *.* TO 'NewUser'@'localhost';
FLUSH PRIVILEGES;
```
Drop User:
------------
```
DROP USER 'fooder_dev'@'localhost';
```
import
----------
```
mysqldump -uroot -p db_name < db.sql
```
on mac
```
mysql -uroot -p db_name < db.sql
```

esport
----------
```
mysqldump -uroot -p db_name > db.sql
```

ssh download file
------------------
with ssh key
```
scp hostname:/remote/dir/foobar.txt /local/dir
```
with .pem file
```
scp -i key_file.pem your_username@remotehost.edu:/remote/dir/foobar.txt /local/dir
```
