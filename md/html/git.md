#GIT工具的快速使用
	
##安装
	
请到官网 <a href="git-scm.com">git-scm.com</a> 或国内的下载站，下载安装包。
	
##创建项目有两种情况
	
1.本地无项目，克隆远程库的文件到本地 例如在github或oscgit上已有的项目，可以将其拉取到本地上
	
```
git clone  https://github.com/angular/quickstart  my-projName
cd my-projName
```
注意：上面的git clone命令需要传入第一个参数是远端git库的地址，第二个参数是本地的项目名字（也就是本地的文件夹名称）
	
1.本地有项目，合并远程库的文件到本地 例如我本地开发好一个程序应用，并且在github或oscgit上创建好一个空的库，需要把代码上传到该库
	
2.首先,你需要执行下面两条命令,作为git的基础配置,作用是告诉git你是谁,你输入的信息将出现在你创建的提交中.
```
git config --global user.name "你的名字或昵称"
git config --global user.email "你的邮箱"
```
	
3.那我们第一步可以初始化本地库先
```
//进入到本地程序所在根目录
git init                //git的初始化
```
	
4.给该本地库添加远程库地址
```
git remote add origin <repo-address>        //把远程库的地址填入到<repo-address>
```
	
5.把本地库文件和远程库文件进行合并
```
git pull origin master
```
	
6.添加文件到本地库
```
git add .                            //添加本地队列
git commit -m "第一次提交"            //把队列中的文件提交到本地库
```
	
7.合并后提交代码
```
git push origin master            //把本地库的文件推送到远程库的master主线
```
如果需要账号密码的话就输入账号密码，这样就完成了一次提交。
	
8.设置操作的默认库和分支
```
git branch --set-upstream-to=origin/master
```
##常用的提交操作
1.修改或添加好自己的文件后，需要把文件添加到git队列中
```
git add .        //把当前所有改动后的文件添加到git队列中
```
	
2.把队列中的文件提交到本地库
```
git commit -m "提交说明"
```
尤其注意参数-m ,是必须的，表示提交时的说明文字
	
3.如果该项目存在多人协作，这一步必不可少，有效防止文件冲突
```
git pull
```
这一步会把远程库的文件拉取到本地库，会对有冲突的文件进行自动合并(尽量不要让多人同时改动一个文件，否则自动合并失效，需要手动合并)
	
```
git pull origin master  //表示拉取所设源地址的主线分支代码
```
有可能提示说找不到要拉取的远端地址，可以在命令后面添加参数
	
4.最后保证上面几步没问题后，把本地库文件推送到远端库
```
git push
```
有可能提示说找不到要拉取的远端地址，可以在命令后面添加参数
```
git push origin master  //表示推送到所设源地址的主线分支
```
	
##解决冲突
	
在提交时可能会存在冲突，所谓的冲突，就是你跟你的基友在修改同一个文件的同一行的内容时，系统无法判断用谁的代码。
	
当你使用git pull的时候，会有冲突提示
	
<img src="../../media/git1.png" />
	
这个时候，我们的git会自动把冲突位置显示在相关文件里
	
<img src="../../media/git2.png" />
	
二选一，要么留自己的代码，要么留别人的代码，编辑完成后，再重新四步走。
	
当然，某些特殊情况，需要强制推送的话，执行下面的命令
```
git push origin master -f
```
如果您选择保留线上的readme文件,则需要在提交前先执行
```
git pull origin master
```
拉取的时候，Git自动合并，并产生了一次提交。<br />
如果不能够自动合并，那么会提示
##提交时老是提示输入用户名密码
```
git config --global credential.helper store
```
执行完后，下次提交再次输入账号密码，即可以自动存储了
##查看git库的当前状态
```
git status
```
##还原修改git checkout
	
让文件回到最近一次git commit或git add时的状态
```
git checkout -- index.html
```
##如果遇到以下情况，无法add和commit
```
On branch master
Your branch is up-to-date with 'origin/master'.
Changes not staged for commit:
        modified:   ../index.html

no changes added to commit
```
上面这种情况，其实是因为你改变了index文件，但并没有有效的add到暂存区中，需要检查自己是否有把该文件有效的git add。
	
根据多年经验，其实往往可能是因为我们cd到了子目录，然后再执行git add ./，从而导致修改的文件，并没有真正的添加进去)
##fatal:multiple stage entries for merged file
```
解决办法如下：
1.执行rm .git/index，回车
2.执行git add -A，回车
3.git commit -m "您的修改说明"
```
##时光穿梭
1.先查看要回退的时间点
```
git log
```
<img src="../../media/time.png" />
	
2.根据ID回退到历史的某一个时间
```
git reset --hard d48bf2fcd99
```
hard的参数值就是第一步所获取到的id(不需要全部，可以截取其中一截就可以了)、