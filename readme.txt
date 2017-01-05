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

lesson_4:


