# Github 使用指南
git status -s  
查看当前路径下本地文件的git状态

git log  
git log --oneline
只输出简单的commit的名字和简写MD5

git add .  

git show xxxxxxxxxxxxxxx（commit码）  

git commit -m "description"  

## git push
[参考博客](http://www.cnblogs.com/qianqiannian/p/6008140.html)  
git push <远程主机名> <本地分支名>  <远程分支名>  

git push origin master  
如果远程分支被省略，如上则表示将本地分支推送到与之存在追踪关系的远程分支（通常两者同名），如果该远程分支不存在，则会被新建

git branch [name] [start point]
创建新分支
git branch --set-upstream master origin/master  
Git新建本地分支与远程分支关联

git remote

git checkout [-q] [<commit>] [--] <paths>
把文件回滚？（省略commit的话，工作区文件就会被本地缓存区文件覆盖）（--是为了避免commit和path重名而引发歧义）
（commit既可以是某一个具体的commit hash值，也可以是某个分支名称，tag名称。不论分支也好，tag也好，它们本质上对应的都是一个commit hash值（hash值不用写全，简写即可）。）
git checkout [<branch>]
切换到新分支
git checkout [-m] [ [-b | -- orphan ] <new_branch>]  [start_point] 
（--orphan 它会基于当前所在分支新建一个赤裸裸的分支，没有任何的提交历史，但是当前分支的内容一一俱全）
（-b 新建分支，-B 强制新建分支（如果有同名分支则直接覆盖） ）
git checkout --merge <branch>
这个命令适用于在切换分支的时候，将当前分支修改的内容一起打包带走，同步到切换的分支下。（容易产生冲突，慎用）
git checkout -p <branch>
这个命令可以用来打补丁。这个命令主要用来比较两个分支间的差异内容，并提供交互式的界面来选择进一步的操作。
git checkout --orphan gh-pages
创建没有父节点的分支gh-pages。因为github规定，只有该分支中的页面，才会生成网页文件。（12年的数据，待更新）

git config --global credential.helper store  
配置让GIT记住密码账号。  