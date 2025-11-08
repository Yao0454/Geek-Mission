# Git进阶
其实就是我之前整理的常用命令
```Git
//首先肯定是我们的git clone啦

git clone "仓库地址"

//其次是一些初始化以及配置的命令

git init //初始化一个本地仓库

git config --global user.name "用户名" //设置全局用户名
git config --global user.email "你的邮箱" //设置全局邮箱

git config --list //列出Git的所有配置

//然后是文件操作

git add file_name //给文件添加到暂存区
git add . //将目录下所有修改添加到暂存区

git commit -m "Text" //commit你的更改 Text是写提交时的注释

git rm file_name //删除文件

//然后是分支管理

git branch //查看仓库里的所有分支
git branch name //创建新的分支
git branch -d name //删除分支

git checkout name //切换到name的分支
git checkout -b name //整合上两个的操作 创建并切换到新的分支

git merge name //合并指定分支

//然后是远程管理

git remote -v //查看仓库地址
git remote add origin "仓库地址" //添加远程仓库

git push //推送当前分支到远程仓库
git push -u origin "branch_name" //将本地分支push到远程仓库

git pull //pull远程仓库并合并

git fetch //pull远程仓库但不合并

//怎么挂代理服务器

git config --global proxy.http "代理服务器地址"
git config --global proxy.https "代理服务器地址"
```