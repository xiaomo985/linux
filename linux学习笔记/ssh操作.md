1. 安装ssh服务器：`sudo pacman -S openssh`
2. 检查ssh服务状态：`sudo systemctl status sshd`
3. 启动ssh服务：`sudo systemctl start sshd`
4. 设置防火墙：
	1. 安装`ufw`管理防火墙：`sudo pacman -S ufw`
	2. 启动并允许ssh流量：
		```
			sudo ufw enable
			sudo ufw allow ssh	
		```
5. 连接ssh服务器：`ssh 用户名@服务器IP地址`
6. 