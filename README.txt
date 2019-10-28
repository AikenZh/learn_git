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

