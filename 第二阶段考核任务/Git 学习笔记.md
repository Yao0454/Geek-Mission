# Git的学习

在 Linux 环境下， 安装 Git 非常简单，只需要
``` Shell
sudo apt install git 
```
就可以了  

首先设置全局用户名和邮箱
``` Shell
git config --global user.name "Yao0454"
git config --global user.email "yaoyifeng20070524@outlook.com"
```
然后在仓库中，创建一个 hello.md 的文件
``` Shell
vim ./hello.md
```
![[Pasted image 20251107154832.png]]
输入
``` Shell
# Hello + 姚奕枫
```
然后使用 Git ，输入
``` Shell
git add .
//用来将文件添加到暂存区

git commit -m "hello.md"
//用来提交修改

git push -u origin main
//推送修改到main分支

```
![[Pasted image 20251107161236.png]]
看到这样就说明成功了
