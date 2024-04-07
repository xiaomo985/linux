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
6. 用不同的端口号连接：`ssh -p 端口号 用户名@ 服务器IP地址`
7. 传输文件：
	1. 使用SCP命令在将本地计算机文件发送到远程服务器：`scp /path/to/local/file 用户名@remote_host:/path/to/remote/directory`
	2. 使用SCP命令在将远程服务器文件发送到本地计算机：`scp 用户名@remote_host:/path/to/remote /path/to/local/directory`
8. 配置ssh密钥认证：
	1. 检查ssh密钥是否存在：`ls ~/.ssh`
	2. 生成密钥对：`ssh-keygen -t rsa -b 4096`
	3. 保存密码，将公钥（`id_rsa.pub`文件）添加到服务器`~/.ssh/authorized_keys`文件中：`ssh-copy-id 用户名@remote_host`