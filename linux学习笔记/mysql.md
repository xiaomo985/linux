1. 登陆
	1. 登陆本地mysql账户`mysql -u root -p`
	2. 登陆远程mysql账户`mysql -u root -p -h hostname`
	3. 密码`ABC123@abc123`
2. 启动数据库
	1. 启动数据库：`sudo systemctl start mysql`
	2. 开机启动数据库：`sudo systemctl enable mysql`
3. 数据库操作
	1. 创建数据库：`CREATE DATABASE mydatabase；`
	2. 删除数据库：`DROP DATABASE mydatabase;`
	3. 使用数据库：`USE mydatabase;`
	4. 显示所有数据库：`SHOW DATABASES;`
4. 表格操作
	1. 创建表格：`CREATE TABLE 表格名;`
	2. 删除表格：`DROP TABLE 表格名;`
	3. 显示表格结构：`DESCRIBE 表格名；`或者`SHOW COLUMNS FROM 表格名;`
5. 数据操作
	1. 查询数据：`SELECT * FROM 表格名;`
	2. 更新数据：`UPDATE 表格名 SET 数据 WHERE 条件;`
	3. 删除数据：`DELETE FROM 表格名 WHERE 条件;`
	4. 插入数据：`INSERT INTO 表格名 VALUES;`
6. 数据库用户操作
	1. 创建数据库用户：`CREATE USER '用户名'@'主机名'IDENTIFIED BY '密码'；`
	2. 删除用户：`DROP USER '用户名'@‘主机名’；`
	3. 授予数据库用户权限：`GRANT ALL PRIVILEGES ON mydatabase.* TO '用户名'@‘主机名’；`
	4. 撤销权限：`REVOKE PRIVILEGES ON 数据库名.* FROM '用户名'@‘主机名’； `
	5. 刷新权限：`FLUSH PRIVILEGES;`
7. 备份
	1. 备份整个数据库：`mysqldum -u 用户名 -p 数据库名 > backup.sql`
	2. 恢复整个数据库：`mysql -u 用户名 -p 数据库名 < backup.sql`
8. 退出数据库控制台：`exit;`
