---
git 教程
---
#### 配置git
git config -global user.name "名字"			每次提交时显示的用户名
git config -global user.emali "邮箱"			 每次提交时显示的邮箱
#### 格式化仓库
git init
#### 新建文件添加到暂存区
mkdir　目录名		   	创建目录
cd 目录名　　　　　进入目录
vim 文件名　　　　  创建文件
git add 文件名　　　添加到暂存区　　
git add . 						   所有文件添加到暂存区
git status   					 查看暂存区状态
#### 添加到本地仓库
git commit -m "说明"　　添加到本地仓库
git status								   查看本地仓库状态
#### 修改文件
vim 要修改的文件
git diff  文件名					查看修改了什么内容
git cat									  查看文件里的内容
git add 文件名　　   		添加到暂存区
git status								查看暂存区状态
git commit -m "说明"　 添加到本地仓库
#### 版本回退
git log									                  查看提交过的所有版本的详细日志
git log --pretty=oneline                查看提交过的所有版本的日志在一行显示
git log --online                                  显示提交过的所有的简介版本号
git reflog                                             显示提交过的所有版本　显示到需要的版本需要几步
git reset --hard 版本号　　　　 回退到需要的版本号
git reset --hard HEAD^                  回退１个版本　　几个＾几个版本
git reset --hard HEAD～３			  回退３个版本　　数字是几回退几个版本
git add 文件名　　　					   提交到暂存去
git commit -m "说明"　　　　  提交到本地仓库
git diff 文件名                                   查看修改的内容
git diff HEAD                                    跟本地库的所有版本比较
git diff HEAD^                                  跟本地库的上一个版本比较
git checkout -- 版本号                  版本撤回
git reset  HEAD 文件名                  把暂存去的撤销到工作区
git checkout 文件名                      删除工作区的文件
#### 远程仓库
git remote add 名字 git@github.com:guobing123123/learngit.git              关联远程仓库
git push -u 名字 master                                          第一次加u 推送到远程仓库  以后不用                             
#### 克隆
git clone 仓库地址                            克隆远程仓库
git remote -v                                      查看克隆内容的别名
#### 分支管理
git checkout -b 分支名         创建分支并切换
git branch   分支名                    创建分支
git checkout 分支名                  切换分支
git merge 分支名                       合并某分支到当分支
git branch -v                                查看所有的分支
git status                                       查看在哪支上
git branch -d 分支名                 删除分支
git branch -D 分支名                 强制删除分支
#### bug分支
git stash   隐藏分支
git stash list  查看隐藏分支
git stash pop 显示隐藏的分支
git merge --no-ff -m "merge with no-ff" 文件名      准备合并文件分支，请注意--no-ff参数，表示禁用Fast forward
#### 多人协作
查看远程库信息，使用git remote -v；
本地新建的分支如果不推送到远程，对其他人就是不可见的；
从本地推送分支，git push origin branch-name，如果推送失败，先用git pull抓取远程的新提交；
在本地创建和远程分支对应的分支，使用git checkout -b branch-name origin/branch-name，本地和远程分支的名称最好一致；
建立本地分支和远程分支的关联，使用git branch --set-upstream branch-name origin/branch-name；
从远程抓取分支，使用git pull，如果有冲突，要先处理冲突。
#### 查看秘钥
cd.ssh 进入公钥秘钥存放的目录    
vim id_rsa.pub 进入公钥 
ssh-keygen -t rsa -C 用户名
ll   查看目录
cat id_rsa     查看文件	
复制公钥
填写到网站上
#### 标签管理
git checkout 分支名                        切换到要打标签的分支上
git tag  标签名                                  打标签
git tag                                                 查看所有的标签
git show 标签名                                          查看标签的信息
git tag -a 标签名 -m "说明" 版本号      带有说明的标签
git push 名字 标签名                              推送到远程仓库
git push 名字 --tags                               推送全部标签到远程仓库
git tag -d 标签名                              删除本地标签
git push origin :refs/tags/标签名     删除远程仓库标签

