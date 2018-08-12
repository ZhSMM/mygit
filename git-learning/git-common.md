# git常用的命令
## 初始化
1. git init +filepath：创建文件目录并生成.git版本控制文件。
2. git config --global/--local user.name/user.email: 设置基本的信息（全局或本地，本地优先级高于全局）
3. git config --list：查看所有设置

## git常用命令
1. mkdir: XX （创建一个空目录，XX指目录名）
2. pwd：当前目录的路径
3. git add XX：把XX文件添加到暂存区去
4. git commit -m ‘提交说明’：提交确认
5. git status：查看仓库状态
6. git diff XX：查看XX文件修改了哪些内容
7. git log：查看历史记录
8. git reset —hard HEAD^^/HEAD~n：回退到前2或n个版本
9. cat XX：查看XX文件内容
10. git reflog：查看历史记录的版本号
11. git checkout - XX：把XX文件在工作区的修改全部撤销
12. git rm XX：删除XX文件

## 关联远程库
1. git remote add origin git@github.com:ZhSMM/mygit.git ：关联一个远程库
2. git push -u（第一次要用-u，以后不需要）origin master：把当前master分支推送到远程库
3. git clone git@github.com:ZhSMM/mygit.git：从远程库中克隆
4. git checkout -b dev:创建Dev分支，并切换到Dev分支上
5. git branch：查看当前所有分支
6. git checkout master:切换回master分支
7. git merge Dev：在当前的分支上合并Dev分支
8. git branch -d Dev：删除Dev分支
9. git branch name：创建分支
10. git stash：把当前的工作隐藏起来，等以后恢复现场继续工作
11. git stash list：查看被隐藏起来的文件列表
12. git stash apply：恢复被隐藏的文件，但内容不删除
13. git stash drop：删除文件
14. git stash pop：恢复文件的同时，也删除文件
15. git remote：查看远程库的消息
16. git remote -v：查看远程库的详细信息
17. git push origin master：把master分支推送到对应的远程分支上