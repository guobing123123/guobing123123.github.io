---
layout: post
title: iOS开发中的小问题记录
date: 2016-12-02 
tag: iOS
---

git status   查看工作区.暂存区的状态
git add 文件名  将工作区的新建/修改存储到暂存区
git cat  查看文件里的内容
git commit -m "注释"  将暂存区的内容提交到本地库
git log  显示最完整的版本号
git log --pretty=oneline  显示完整的版本号
git log --online   显示最简洁的版本号
git reflog   显示版本号    显示到哪个版本需要移动几步
git reset --hard 版本号     回退到需要的版本号
git reset --hard HEAD^    回退1个版本    ^^两个几个符号就是几个不能前进只能后退
git reset --hard HEAD~2    回退2个版本   ~10 回退10个版本    数字是几回退几个  只能后退
git reset --hard 版本号   在本地库找回版本号
rm 文件名   删除本地库文件    //找回文件
git add 文件名  提交到暂存区
git commit -m "" 提交到本地库    
git diff 文件名    查看修改的内容  
git diff HEAD      跟本地库的版本比较
git diff HEAD^   跟本地库上一个版本比较
git checkout -- 版本撤回

#### 分支***

1. git status 查看在哪个分支上

2. git branch -v  查看所有的分支

3. git branch  分支名      创建一个分支

4. git checkout  分支名      切换分支

5. 合并分支  切换到接受修改的分支上

6. 把修改的内容合并到合并到主分支上    默认分支是主分支

7. git merge  分支名    合并分支    分支名写要合并的分支

8. get checkout -b 分支名      新建分支并切换

   分支管理策略

   1. git checkout -b 分支名 新建分支并且切换
   2. git add  文件名
   3. git commit 文件名
   4. git merge --no-ff -m "merge with no-ff" 文件名      准备合并文件分支，请注意--no-ff参数，表示禁用Fast forward
   5. git log 查看版本号
   6. git stash   隐藏文件   维修完   
   7. git stash pop   找到隐藏文件\
   8. git branch -d 分支名    删除分支
   9. git branch -D 分支名     删除不了强制删除

   

#### 分支冲突

1.git add 文件名   解除冲突
2.git status  查看分支状态
3.git commit -m  ""       结束分支

#### 添加远程仓库

1.git remote add origin git@github.com:guobing123123/learngit.git    本地仓库关联远程仓库
2.git push -u origin master                     把本地仓库推送到远程库ls

#### 克隆 

git@github.com:guobing123123/aihuan.gitgit config --list  查看设置过的参数	
git clone 地址      从远程仓库克隆文件到目录
git remote -v  查看克隆内容的别名
           初始化本

git fetch 远程库地址名   远程分支名

git checkout远程库地址名/远程分支名的内容   cat 文件名

git push -u 名字 要推送的分支名  推送到仓库





cd.ssh 进入公钥秘钥存放的目录    

vim id_rsa.pub 进入公钥 

ssh-keygen -t rsa -C 用户名

ll   查看目录

cat id_rsa     查看文件	

复制公钥

填写到网站上