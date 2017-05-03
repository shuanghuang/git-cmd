初始化仓库
$ git init

配置 信息
$ git config --global user.name shuanghuang
$ git config --global user.email

查看隐藏git文件
$ ls -ah

$ vi readme.txt

把文件添加到暂存区
$ git add readme.txt

从版本库中删除该文件
$ git rm test.txt

把暂存区的所有内容提交到当前分支
$ git commit -m "commit a test file"

查看当前状态
$ git status

查看修改内容
$ git diff version1(HEAD) version2 -- readme.txt

查看版本记录日志
$ git log --pretty=oneline

回退版本
$ git reset --hard HEAD^(^^^^^^)||HEAD~100
$ git reset --hard c922f7cb65a3296e5666503d4231b88e24c027fd

把暂存区的修改撤销掉（unstage）
git reset HEAD readme.txt

每一次命令日志
$ git reflog

丢弃工作区的修改
$ git checkout -- readme.txt


远程仓库

关联一个远程库
$ git remote add origin git@github.com:shuanghuang/studygit.git

提交
$ git push (-u) origin master

$ git checkout -b dev

创建分支
$ git branch dev
切换分支
$ git checkout dev

查看当前分支
$ git branch 

合并指定分支到当前分支
$ git merge dev

删除dev分支
$ git branch -d dev

创建功能分支：
　　git checkout -b feature-x develop
开发完成后，合并到develop分支：
　　git checkout develop
　　git merge --no-ff feature-x
最后删除分支:
　　git branch -d feature-x

git push origin --delete develop

禁用fast-forward
$ git merge --no-ff -m "merge with no-ff" dev

看看分支历史
$ git log --graph --pretty=oneline --abbrev-commit

把最新的提交从origin/dev抓下来
$ git pull

拉取远程分支到本地
git checkout -b dev origin/dev

提交到dev分支
git push origin dev

指定本地dev分支与远程origin/dev分支的链接
git branch --set-upstream dev origin/dev
