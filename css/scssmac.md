#Sass苹果安装

#步骤0 － 安装系统需要的包
　# For Mac 　　# 先安装 [Xcode](https://developer.apple.com/xcode/) 开发工具，它将帮你安装好 Unix 环境需要的开发包

#步骤1 － 安装 RVM
RVM 是干什么的这里就不解释了，后面你将会慢慢搞明白。
```
$ curl -L https://get.rvm.io | bash -s stable
```
期间可能会问你sudo管理员密码，以及自动通过homebrew安装依赖包，等待一段时间后就可以成功安装好 RVM。<br/>
然后，载入 RVM 环境（新开 Termal 就不用这么做了，会自动重新载入的）
```
$ source ~/.rvm/scripts/rvm
```
检查一下是否安装正确
```
$ rvm -v
rvm 1.26.11 (latest) by Wayne E. Seguin <wayneeseguin@gmail.com>, Michal Papis <mpapis@gmail.com> [https://rvm.io/]
```
#步骤2 － 用 RVM 安装 Ruby 环境
列出已知的ruby版本
```
$ rvm list known
```
可以选择现有的rvm版本来进行安装（下面以rvm 2.2.1版本的安装为例）
```
$ rvm install 2.2.1
```
同样继续等待漫长的下载，编译过程，完成以后，Ruby, Ruby Gems 就安装好了。<br/>
另附：<br/>
查询已经安装的ruby<br/>
```
$ rvm list
```
卸载一个已安装版本
```
$ rvm remove 1.9.2
```
#步骤3 － 设置 Ruby 版本
RVM 装好以后，需要执行下面的命令将指定版本的 Ruby 设置为系统默认版本
```
$ rvm 2.2.1 --default
```
同样，也可以用其他版本号，前提是你有用 rvm install 安装过那个版本<br/>
这个时候你可以测试是否正确
```
$ ruby -v
ruby 2.2.1p85 (2015-02-26 revision 49769) [x86_64-darwin15]

$ gem -v
2.4.8
```
#步骤4 － 切换淘宝RubyGems镜像
这有可能是因为Ruby的默认源使用的是cocoapods.org，国内访问这个网址有时候会有问题，网上的一种解决方案是将远替换成淘宝的，替换方式如下：
```
$ gem source -r https://rubygems.org/
$ gem source -a https://ruby.taobao.org
```
要想验证是否替换成功了，可以执行：
```
$ gem sources -l
```
正常的输出结果：
```
CURRENT SOURCES　　

http://ruby.taobao.org/
```
到这里就已经把Ruby环境成功的安装到了Mac OS X上，接下来就可以进行相应的开发使用了。
#步骤5 － sass安装
在命令行中输入
```
gem install sass
```
查看sass版本
```
sass -v
```
这样便把sass安装完成。