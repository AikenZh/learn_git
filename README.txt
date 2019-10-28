learning git.
need more practice.

git init

git add file

git commit -m '提交说明'
	-a 无需add直接提交

git status
	-s: 简短输出

git diff
	未添加至暂存区的改动
	暂存区文件 对比 版本库文件：--cached
	工作区文件 对比 版本库文件：HEAD
	显示摘要：--stat

git reset HEAD <file>
	取消已缓存的文件

git rm file
	强制删除: -f
	只删除暂存区的文件: --cached
	递归删除: -r

git mv 
	用于移动、重命名

git checkout --file
	撤销暂存区的修改，也可从版本库恢复误删

git branch
	查看分支

git branch branchname
	创建分支

git checkout branchname 或 git switch branchname
	切换分支

git checkout -b branchname 或 git switch -c branchname
	创建并切换到分支

git merge branchname
	合并分支
	禁用Fast forward以便查看分支历史: --no-ff

git branch -d branchname
	删除分支

git log
	显示2行: -2
	查看简介日志: --oneline
	开启拓扑图，查看分支合并历史: --graph
	逆向显示: --reverse
	查看指定用户的提交日志: --author=name
	查看指定日期: --since --before --after --until
	    如: git log --oneline --before={3.weeks.ago} --after={2010-04-18}

