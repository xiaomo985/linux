登陆本地mysql账户`mysql -u root -p`
登陆远程mysql账户`mysql -u root -p -h hostname`
密码`ABC123@abc123`
启动数据库：`sudo systemctl start mysql`
开机启动数据库：`sudo systemctl enable mysql`
创建数据库：`CREATE DATABASE mydatabase；`
删除数据库：`DROP DATABASE mydatabase;`
使用数据库：`USE mydatabase;`
显示所有数据库：`SHOW DATABASES;`
创建表格：`CREATE TABLE 表格名;`
删除表格：`DROP TABLE 表格名;`
显示表格结构：`DESCRIBE 表格名；`或者`SHOW COLUMNS FROM 表格名;`
插入数据：`INSERT INTO 表格名 VALUES;`
查询数据：`SELECT * FROM 表格名;`
更新数据：`UPDATE 表格名 SET 数据 WHERE 条件;`
删除数据：`DELETE FROM 表格名 WHERE 条件;`
创建数据库用户：`CREATE USER '用户名'@'主机名'IDENTIFIED BY '密码'；`
删除用户：`DROP USER '用户名'@‘主机名’；`
授予数据库用户权限：`GRANT ALL PRIVILEGES ON mydatabase.* TO '用户名'@‘主机名’；`
撤销权限：`REVOKE PRIVILEGES ON 数据库名.* FROM '用户名'@‘主机名’； `
刷新权限：`FLUSH PRIVILEGES;`
备份整个数据库：`mysqldum -u 用户名 -p 数据库名 > backup.sql`
恢复整个数据库：`mysql -u 用户名 -p 数据库名 < backup.sql`
推出数据库控制台：`exit;`
