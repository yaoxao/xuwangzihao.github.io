# Github 使用指南
git status -s  
查看当前路径下本地文件的git状态

git log  

git add .  

git show xxxxxxxxxxxxxxx（commit码）  

git commit -m "description"  

## git push
[参考博客](http://www.cnblogs.com/qianqiannian/p/6008140.html)  
git push <远程主机名> <本地分支名>  <远程分支名>  

git push origin master  
如果远程分支被省略，如上则表示将本地分支推送到与之存在追踪关系的远程分支（通常两者同名），如果该远程分支不存在，则会被新建

git branch [name]  
git branch --set-upstream master origin/master  
git remote


git config --global credential.helper store  
配置让GIT记住密码账号。  