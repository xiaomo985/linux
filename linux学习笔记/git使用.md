1. 常用命令
	1. 初始化一个目录：` git init`
	2. 初始提交：`git add +文件名`将文件提交到暂存区；`git commit `将文件正式提交；`git commit --amend`撤销操作
	3. 检查配置文件：`git config --list`
	4. 查看配置好的远程仓库：`git remote -V`
	5. 克隆仓库：`git clone +网址 +（自定义文件名）`
	6. 检查文件状态：`git status`；新文件需要配合`git add +文件名`命令才能检查文件状态
	7. 查看文件变动了那些：`git diff`
	8. 删除暂存区文件：`git rm +文件名`
	9. 改文件名：`git mv 原文件名 新文件名`
	10. 查看提交历史：`git log`
	11. 查看已配置的远程仓库：`git remote`
	12. 添加远程仓库：`git remote add 新名字 网址`
	13. 从远程仓库抓取：`git fetch +网址`
	14. 推送到远程仓库：`git push 远程仓库名 分支名`
	15. 打上版本标签：`git tag "标签"`
2. 配置方法
	1. 生成ssh密钥：`ssh-keygen -t rsa -b 4096 -C "xiaomo985@outlook.com"`
	2. 保存路径为`/home/like/.ssh/id_rsa`
	3. 添加密钥到ssh-agent：
		1. 后台启动`ssh-agent`：`eval "$(ssh-agent -s)"`
		2. 添加已经生成的密钥：`ssh-add /home/like/.ssh/id_rsa`
		3. 添加密钥到github账户：
			1. 复制密钥`cat /home/like/.ssh/id_rsa`；
			2. 粘贴命令行密钥到github如下图
				![[github_ssh.png]]	
3. 22端口可能会被防火墙屏蔽
	1. 创建一个config文件: `vim ~/.ssh/config`
	2. 写入下面内容:
		1. ```Host github.com
			Hostname ssh.github.com
			Port 443```
		