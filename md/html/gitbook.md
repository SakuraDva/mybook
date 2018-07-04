#Gitbook 的使用和常用插件
    
    
    
#Gitbook 介绍

<h6>Gitbook 是基于 Node.js 的命令行工具，用来创建漂亮的电子书，它使用 Markdown 或 AsciiDoc 语法来撰写内容，用 Git 进行版本控制，且可以托管在 Github 上。Gitbook 可以将作品编译成网站、 PDF、 ePub 和 MOBI 等多重格式。<h6>
    
<h6>如果你不擅长自己搭建 gitbook 环境，还可以使用 gitbook.com 在线服务来创建和托管你的作品，他们还提供了基于桌面的 编辑器 

#如何使用
1.首先在全局安装 gitbook 客户端工具：
    
```npm install gitbook-cli -g```
    
2.创建book.json并安装 创建一个空的文件夹，并在这个文件夹中创建一个book.json文件
    
```
 {
"gitbook":"2.x.x"
 }
 ```
    
表示安装gitbook的2.x.x版本，以后可以扩展此文件安装更多的gitbook插件
    
```
 gitbook install
```
    
3.创建README.md 和 SUMMARY.md
    
```
gitbook init
```
在你的作品目录中创建两个必需的文件 README.md 和 SUMMARY.md，README.md 是作品的介绍，SUMMARY.md 是作品的目录结构，里面要包含一个章节标题和文件索引的列表：
    
```
# Summary

 This is the summary of my book.

 * [section 1](section1/README.md)
     * [example 1](section1/example1.md)
     * [example 2](section1/example2.md)
         - [example 3](section1/example3.md)
 * [section 2](section2/README.md)
     * [example 1](section2/example1.md)
```
4.运行服务，在编辑内容后实时预览：
    
```
gitbook serve
```
服务器启动后，浏览器打开 http://localhost:4000 查看
5.撰写完后可以生成静态网站用来发布：
    
```
 gitbook build
```
6.更多命令帮助
    
```
 gitbook help
```
7.自由切换版本
    
```
gitbook ls-remote           //罗列出所有的版本号
gitbook fetch 2.1.0         //选择其中一个版本切换安装
```
8.更多插件 参考链接[https://www.tuicool.com/articles/zee2ui]
    
#Gitbook常用插件介绍
    
想要添加gitbook配置或插件，只需要在book.json里面添加即可
###示例代码
    
```
   {
        "gitbook" : "2.x.x",
        "title":"学习笔记",
        "author":"Bluej",
        "plugins":[
            "sectionx",
            "expandable-chapters"
        ]
}
```
    
1.配置
    
|键名|描述|代码| 
|:-|:-|:-| 
|title|设置书本的标题|"title" : "学习笔记"| 
|author|作者的相关信息|"author" : "Bluej"| 
|description|本书的简单描述|"description" : "记录Gitbook的配置和一些插件的使用"|
    

示例代码
```
	  {
		 "title":"学习笔记",
		 "author":"Bluej",
		 "description":"记录Gitbook的配置和一些插件的使用"
	 }
```
    
2.常用插件
    
菜单折叠
    
####expandable-chapters-interactive
```
"plugins": [
         "expandable-chapters-interactive"
     ]
```
    
代码折叠
    
sectionx 将页面分块显示
```
"plugins": [
        "sectionx"
     ]
```
使用方法:在写md笔记时按照下面的语法使用即可
```
<!--sec data-title="Introduction" data-id="section0" data-show=true ces-->

 Insert markdown content here (you should start with h3 if you use heading).

 <!--endsec-->
```
    
3.禁用插件 在插件名字前面添加-表示禁用
```
 "plugins":[
         "-sectionx",//禁用sectionx插件
         "expandable-chapters"
     ]
```
####更多插件介绍请参考 这里[http://blog.csdn.net/qq_37149933/article/details/64170653]