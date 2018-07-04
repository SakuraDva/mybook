#Sass的使用

#什么是Sass
sass这个语言的诞生，主要用于更好的编写和维护我们的css代码<br/>
 可以理解为超级css（它的文件后缀名为.scss）
#为什么要用Sass
因为它具备很多编程语言的特点在里面，例如代码可以封装为模块，进行重组，也可以对我们的结构进行有条不紊的编排，这些都是原来的css所做不到的。并且，面对日益复杂的网站和需求，多人协作已经是一个趋势，让我们用sass可以更好的去协同多人代码的分工和合并。
#什么时候用Sass
当你要写css的时候
##例如
```
<html>
	<head>
		<meta charset="utf-8" />
		<title></title>
		<link rel="stylesheet" type="text/css" href="css/index.css"/>
	</head>
	<body>
		<!--
			Sass语言-预处理CSS
			
			1.#what他是个什么东西
			   sass这个语言的诞生，主要用于更好的编写和维护我们的css代码
			   可以理解为超级css（它的文件后缀名为.scss）
			2.why  为什么要用它
			  因为它具备很多编程语言的特点在里面，例如代码可以封装为模块，进行重组，也可以对我们的结构进行有条不紊的编排，这些都是原来的css所做不到的。并且，面对日益复杂的网站和需求，多人协作已经是一个趋势，让我们用sass可以更好的去协同多人代码的分工和合并。
			3.when -什么时候用它
			当你要写css的时候
		-->
		
		<!--
			sass安装
			1.ruby安装，安装好用“gem -v”检验是否成功
			2.sass安装，安装好用“scss -v”检验是否成功
			
			使用部分
			有不懂看[文档]（https://www.sass.hk/docs/ ）
			
			开启监听
			scss --watch --style compressed 监听目录：输出目录
			例如
			scss --watch --style compressed scss：css
			
			#语法
			//设置变量，方便后续重复使用，并方便统一修改
				$h1-size:20px;
				$h2-size:18px;
				div .title{
				    font-size: $h1-size;
				}
				
				p .title{
				    font-size: $h1-size;
				}
            #嵌套
            .web{
            	width:1000px;
            	margin:0 auto;
            	header{
            		//这里就可以写关于.web里面的子元素header的相关样式
            		
            	}
            }
            > PS：这样的写法可以方便我们管理元素的层级关系，更好的维护代码
            如果要写伪类选择器和伪对象选择器，可以用“&”来代替自身，例如
            ```
            div{
            	&:hover{
            		background:skyblue;
            	}
            	&::after{
            		content:"";
            	}
            	~p{
            		color:pink;
            	}
            }
            ```
            target选择器是配合锚点使用的
            header{
              &:target{
               border: 15px dotted yellow;
              }
}
            <header id="header"></header>
		    <a href="#header">点我</a>
		    
		    #导入scss文件
		    可以把多次重用的样式写到单独一个scss文件里面，在需要的时候导入进来
		   ```
		    //导入其他scss文件
			@import "common/common";
			@import "common/reset";
			
			div{
			    color: white; 
			}
		   ```
		   > 如果你不希望被导入的文件，被编译成css文件，可以在它的名字掐年加一个**_(下划线)**
		-->
        <div class="title1">
        	
        </div>
        <div class="title2">
        	
        </div>
		<div>
			<p>233333333333333333333</p>
		</div>
		<p>233333333333333333333</p>
		<header id="header"></header>
		<a href="#header">点我</a>
		
		<div class="tag_wrap">
			<a href="#tag1">选项卡1</a>
			<a href="#tag2">选项卡2</a>
			<a href="#tag3">选项卡3</a>
			<div id="tag1">
				选项卡1内容
			</div>
			<div id="tag2">
				选项卡2内容
			</div>
			<div id="tag3">
				选项卡3内容
			</div>
		</div>
		
	</body>
</html>
```