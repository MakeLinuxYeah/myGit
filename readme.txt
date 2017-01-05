Git is a version control system.
Git is free software.

lesson_1:
	初始化一个Git仓库，使用git init命令。
	添加文件到Git仓库，分两步：
		第一步，使用命令git add <file>，注意，可反复多次使用，添加多个文件；
		第二步，使用命令git commit，完成。

lesson_2:
	要随时掌握工作区的状态，使用git status命令。
	如果git status告诉你有文件被修改过，用git diff可以查看修改内容

lesson_3:
	HEAD指向的版本就是当前版本，因此，Git允许我们在版本的历史之间穿梭，
	使用命令git reset --hard commit_id。
	穿梭前，用git log可以查看提交历史，以便确定要回退到哪个版本。
	要重返未来，用git reflog查看命令历史，以便确定要回到未来的哪个版本。

lesson_4:	
	第一步是用git add把文件添加进去，实际上就是把文件修改添加到暂存区；
	第二步是用git commit提交更改，实际上就是把暂存区的所有内容提交到当前分支。

lesson_5:
	Git是如何跟踪修改的，每次修改，如果不add到暂存区，那就不会加入到commit中。

lesson_6:
	场景1：当你改乱了工作区某个文件的内容，想直接丢弃工作区的修改时，用命令git checkout -- file。
	场景2：当你不但改乱了工作区某个文件的内容，还添加到了暂存区时，想丢弃修改，分两步，第一步用命令git
	reset HEAD file，就回到了场景1，第二步按场景1操作。
	场景3：已经提交了不合适的修改到版本库时，想要撤销本次提交，参考版本回退一节，不过前提是没有推送到远程库。

lesson_7:
	删除时：
		场景1：确实要删除，则需要先git rm ，然后再git commit
		场景2：删除错了，则使用git checkout -- file，其实是用版本库里的版本替换工作区的版本，
	无论工作区是修改还是删除，都可以“一键还原”。

lesson_8:
	注册gitHub帐号，
	创建SSH Key，
		ssh-keygen -t rsa -C "youremail@example.com"
	将id_rsa.pub里的内容复制到gitHub中的，“Account settings”，“SSH Keys”页面的“Add SSH Key”中。
	GitHub允许添加多个Key。且对所有人可见。
	
	在验证密钥错误时，输入命令：eval "$(ssh-agent -s)"，然后再次验证即可。
	这里如有报错误：
	To git@git.oschina.net:yangzhi/hello.git
	 ! [rejected]        master -> master (fetch first)
	error: failed to push some refs to 'git@git.oschina.net:yangzhi/hello.git'
	hint: Updates were rejected because the remote contains work that you do
	hint: not have locally. This is usually caused by another repository pushin
	hint: to the same ref. You may want to first merge the remote changes (e.g.
			hint: 'git pull') before pushing again.
	hint: See the 'Note about fast-forwards' in 'git push --help' for details.
	可以输入：
		git push -f 
	可以ok了.

