1. 常用命令
	1. 文件
		列出目录内容`ls -l`
		切换目录`cd 目录名`
		显示当前目录完整路径`pwd`
		复制文件或目录`cp 文件名 新文件名`
		移动文件或目录`mv 文件名 新文件名`
		删除文件或目录`rm -r 目录`递归删除
		创建目录`mkdir 新目录`
		显示整个文件内容`cat 文件名`
		修改文件权限`chmod 777 文件`4：读；2：写；1：运行;
		在文件中搜索指定模式：`grep`
		搜索文件和目录：`find`
		使用数据库快速搜索文件：`locate`
	1. 系统
		显示系统信息`uname`
		显示磁盘空间使用情况`df`
		显示内存使用情况`free`
		实时显示系统资源使用情况`htop`或`top`
		显示当前进程`ps`
		终止进程`kill -9 进程ID`
		终止指定名称所有进程`killall`
		添加用户`useradd`或`adduser`
		修改用户密码`passwd`
		添加用户组`groupadd`或`addgroup`
		查看所有用户账户信息：`cat /etc/passwd | grep '/bin/bash'`
	1. 网络
		测试网络连通性`ping`
		显示和配置网络接口`ifconfig`或`ip`
		显示网络连接和路由表`netstat`
		防火墙常用工具`iptables`用于配置linux内核IPV4数据包过滤规则
		iptables 架构：
			iptables 由多个表（Table）、链（Chain）和规则（Rule）组成。
			表是规则集的容器，每个表都包含一组链，用于定义规则的逻辑分组。
			链是规则的容器，它们决定了什么时候和如何应用规则。
			规则定义了要对网络数据包进行的操作，如接受、拒绝、转发等。
		iptables 表：
			iptables 包括多个预定义的表，其中一些常用的表包括：
			`filter` 表：用于过滤网络流量，通常用于防火墙规则。
			`nat` 表：用于网络地址转换，通常用于实现端口转发、SNAT 和 DNAT 等。
			`mangle` 表：用于修改数据包的特定字段，如 TTL（Time to Live）等。
			`raw` 表：用于配置原始数据包的处理规则。
		iptables 链：
			iptables 包括多个预定义的链，其中一些常用的链包括:
			`INPUT`：处理流入系统的数据包。
			`OUTPUT`：处理流出系统的数据包。
			`FORWARD`：处理通过系统转发的数据包。
		iptables 规则：
			每条 iptables 规则由匹配条件和动作组成。
			匹配条件可以是数据包的来源 IP、目标 IP、协议、端口等。
			动作可以是接受（ACCEPT）、拒绝（REJECT）、丢弃（DROP）、转发（FORWARD）等。
		`iptables`基本命令
			列出当前规则集：`sudo iptables -L`
			清空所有规则：`iptables -F`
			删除用户定义链：`iptables -X`
			将当前规则保存到文件中：`iptables-save`
			从文件中加载规则：`iptables-restore`
			允许特定端口的TCP端口流入流量
			`iptables -A INPUT -p tcp --dport port_number -j ACCEPT`
			允许特定端口的TCP端口流出流量
			`iptables -A OUPUT -p tcp --dport port_number -j ACCEPT`
		持久化：iptables规则在系统重启后重置，需要规则持久化，要把规则保存在文件中，开机加载该文件
		网络端口范围：0到65535；其中0到1023是系统保留的特权端口
		常见端口和对应的服务：
			22：ssh,用于安全远程登陆
			80：HTTP,用于web服务
			443：HTTPS,用于加密web服务
			3306：MySQL数据库服务
			5432：PostgreSQL数据库服务
	将数据由内存同步到硬盘：`sync`
	关机命令：`shutdown -h now`或者`halt`
	重启命令：`shutdown -r now`或者`reboot`
----

1. 配置方法
	1. 输入法配置
	2. 换源
	3. 安装软件
		