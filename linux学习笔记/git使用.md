1. 常用命令
	初始化一个目录
		` git init`
	初始提交
		`git add +文件名`将文件提交到暂存区
		`git commit `将文件正式提交
		`git commit --amend`撤销操作
	克隆仓库
		`git clone +网址 +（自定义文件名）`
	检查文件状态
			`git status`
			新文件需要配合`git add +文件名`命令才能检查文件状态
	查看文件变动了那些
			`git diff`
	删除暂存区文件
			`git rm +文件名`
	改文件名
			`git mv 原文件名 新文件名`
	查看提交历史
			`git log`
	查看已配置的远程仓库
	`git remote`
	添加远程仓库
		`git remote add 新名字 网址`
	从远程仓库抓取
		`git fetch +网址`
	推送到远程仓库
		`git push 网址 文件`
	打上版本标签
		`git tag "标签"`
		
		
1. 配置方法
	生成ssh密钥
		`ssh-keygen -t rsa -b 4096 -C "xiaomo985@outlook.com"`
		保存路径为`/home/like/.ssh/id_rsa`
	添加密钥到ssh-agent
		后台启动`ssh-agent`
		`eval "$(ssh-agent -s)"`
		添加已经生成的密钥
		`ssh-add /home/like/.ssh/id_rsa`
	添加密钥到github账户
		复制密钥
		`cat /home/like/.ssh/id_rsa`
		粘贴命令行密钥到github
		![[github_ssh.png]]
		如上图位置
	22端口可能会被防火墙屏蔽
		`vim ~/.ssh/config`创建一个config文件
		写入下面内容
		```Host github.com
			Hostname ssh.github.com
			Port 443```
		