learning git.
need more practice.

git init

git add file

git commit -m '提交说明'
	-a 无需add直接提交

git status
	-s: 简短输出

git checkout --file
        撤销暂存区的修改，也可从版本库恢复误删

git diff
	未添加至暂存区的改动
	暂存区文件 对比 版本库文件：--cached
	工作区文件 对比 版本库文件：HEAD
	显示摘要：--stat

git reset HEAD file
	取消已缓存的文件

git reset　--hard 版本id\HEAD^
	id为SHA1的前7位即可
	上一个版本，HEAD^ 或 HEAD~1
	上两个版本，HEAD^^ 或 HEAD~2	

git log
        显示n行: -n
        查看简介日志: --oneline
        开启拓扑图，查看分支合并历史: --graph
        逆向显示: --reverse
        查看指定用户的提交日志: --author=name
        查看指定日期: --since --before --after --until
            >> git log --oneline --before={3.weeks.ago} --after={2010-04-18}

git reflog
	查看历史命令

git rm file
	强制删除: -f
	只删除暂存区的文件: --cached
	递归删除: -r

git mv 
	用于移动、重命名

git branch
	查看分支

git branch branchname
	创建分支

git checkout branchname
	切换分支

git checkout -b branchname
	创建并切换到分支

git merge branchname
	合并分支
	禁用Fast forward以便查看分支的历史commit: --no-ff
	   因为包含提交,配合-m使用
	   >> git merge --no-ff -m '提交说明' branchname

git branch -d branchname
	删除分支 若用-D则强制删除

git stash
	暂时'储藏'当前分支到stash栈,以便临时操作其他分支(一般是修改Bug)

git stash list
	查看所有'储藏'的分支

git stash pop
	取出stash,同时删除'储藏'中对应的stash

git stash apply stash@{0}
	取出指定stash,不删除'储藏'中对应的stash

git stash drop stash@{0}
	删除'储藏'中指定的stash

git cherry-pick commit_id
	复制特定的提交到当前分支

git remote add origin url
	添加远程库在本地以origin为别名

git remote
	查看远程库的信息
	详细信息: -v

git push origin master
	将本地master分支和远程master分支关联(第一次push使用)
	将本地master分支推送到远程库

git clone git@github.com:用户名/库名.git
	将远程库克隆至本地,只有master分支
	若在dev分支上开发就要创建远程origin的dev分支到本地
	  >>git checkout -b dev origin/dev

git pull
	将远程库的最新更新取回本地并合并

git fetch
	将远程库的最新更新取回本地需要手动合并


