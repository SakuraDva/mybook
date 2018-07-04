#定位的高级运用


#对齐方法
1. 水平对齐的基本法，缺点是子元素的宽度必须固定
#例子
```
.baba{
	width: 1000px;
	height: 600px;
	position: relative;
	background: skyblue;
}
.son{
	width: 100px;
	height:100px;
	background: white;
	position: absolute;
	/*1. 水平对齐的基本法，缺点是子元素的宽度必须固定*/
	/*left: 50%; */ /*基于父元素的宽度的百分之50偏移*/
	/*margin-left: -50px;*/
```
2. 左右完全居中法
#例子
```
/*left: 0;
right: 0;
margin-left: auto;
margin-right: auto;*/
```
3. 左右上下完全居中
#例子
```
left: 0;
right: 0;
top: 0;
bottom: 0;
margin: auto;
```



```
<html>
	<head>
		<meta charset="UTF-8">
		<title></title>
	</head>
	<body>
		<style type="text/css">
			*{
				margin: 0;
			}
			.baba{
				width: 1000px;
				height: 600px;
				position: relative;
				background: skyblue;
			}
			.son{
				width: 100px;
				height:100px;
				background: white;
				position: absolute;
				/*1. 水平对齐的基本法，缺点是子元素的宽度必须固定*/
				/*left: 50%; */ /*基于父元素的宽度的百分之50偏移*/
				/*margin-left: -50px;*/
				
				/*2.左右完全居中法*/
				/*left: 0;
				right: 0;
				margin-left: auto;
				margin-right: auto;*/
				
				/*3.左右上下完全居中*/
				left: 0;
				right: 0;
				top: 0;
				bottom: 0;
				margin: auto;
			}
		</style>
		<div class="baba">
			<div class="son"></div>
		</div>
		
		<style type="text/css">
			.img_wrap{
				width: 320px;
				height: 250px;
				position: relative;
				border: 10px solid black;
				overflow: hidden;
			}
			.img_wrap img{
				position: absolute;
				left: -999px;
				right: -999px;
				top: -999px;
				bottom: -999px;
				margin: auto;
			}
		</style>
		
		<div class="img_wrap">
			<img src="img/pic.jpg"/>
		</div>
	</body>
</html>
```