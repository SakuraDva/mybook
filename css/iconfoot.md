#iconfoot图标

#icon是什么
在浏览器看来，图片只是一种字,可以在不同分辨率的浏览器下，保持高清，如果用图片的话，在超出图片分辨率的情况下，图片会模糊。
#为什么要用
在实际开发时，过多使用图片会导致页面渲染事件过长，严重影响用户。
#什么时候用
当我们无法用文字展现设计图上色彩斑斓的元素时

#注意
> ps:首选到[阿里图库](http://www.iconfont.cn/)找我们需要的图标。
			1. 先把要用的图标，先添加到库
			2. 把加入到库里的图标，添加至项目中，（好处是可以分模块的管理图标，不会跟其他项目的图标产生冲突）
			3. 把项目下载至本地（默认下载的压缩包叫`downkoad.zip`）
			4. 解压文件，把字体库（.eot,.svg,.ttf,.woff）添加到对应项目的fonts文件夹,把iconfont.css添加到css文件夹。
#reset.css
用来抹平各个浏览器的原始样式。<br/>
让我们制作的页面统一化。

#例子
##引入字体库
<img src="../../media/icon.png"/>
##字体库所存放的文件夹
<img src="../../media/foot.png"/>

```
<html>
	<head>
		<meta charset="utf-8" />
		<title></title>
		<link rel="stylesheet" type="text/css" href="css/iconfont.css"/>
		<style type="text/css">
			.iconfont{
				font-size: 120px;
			}
		</style>
	</head>
	<body>
		<!--
			#what
			在浏览器看来，图片只是一种字,可以在不同分辨率的浏览器下，保持高清，如果用图片的话，在超出图片分辨率的情况下，图片会模糊。
			#when
			当我们无法用文字展现设计图上色彩斑斓的元素时
			#why
			在实际开发时，过多使用图片会导致页面渲染事件过长，严重影响用户。
			> ps:首选到[阿里图库](http://www.iconfont.cn/)找我们需要的图标。
			1.先把要用的图标，先添加到库
			2.把加入到库里的图标，添加至项目中，（好处是可以分模块的管理图标，不会跟其他项目的图标产生冲突）
			3.把项目下载至本地（默认下载的压缩包叫`downkoad.zip`）
			4.解压文件，把字体库（.eot,.svg,.ttf,.woff）添加到对应项目的fonts文件夹,把iconfont.css添加到css文件夹。
			
			reset.css
			用来抹平各个浏览器的原始样式。
			让我们制作的页面统一化。
		-->
		<i class="iconfont icon-wangzherongyao"></i>
	</body>
</html>
```