#class和ID选择器
id 及 class 均是css 提供由用户自定义标签名称的选择符，用户可以使用选择符id及class 来对页面中的xhtml标签进行自定义名称，从而达到扩展xhtml标签及组合html标签的目的。



#id选择器
以id的名字作为目标名，记得前面要加一个#符号。
    
id 选择器可以为标有特定 id 的 HTML 元素指定特定的样式。
    
 注意：一个页面只能存在一个唯一的ID。并不推荐使用，因为后期JS要常用到id这个属性，可能会有冲突。
#class选择器
以class属性所对应的名字作为目标的名字，记得前面加个“.”符号。
    
一个元素可以定义多个class，用空格隔开
    
注意：可以用class来代替id选择器，并且class选择器还可以多次重用，可以更好的控制一个或多个标签。
```
<html>
	<head>
		<meta charset="UTF-8">
		<title></title>
		<style type="text/css">
			/*
			 id 选择器
			 以id的名字作为目标名，记得前面要加一个#符号。
			 注意：一个页面只能存在一个唯一的ID。并不推荐使用，因为后期JS要常用到id这个属性，可能会有冲突。
			 * */
			#p1{
				color: skyblue;
			}
			#p2{
				color: pink;
			}
			/*
			 class 选择器
			 以class属性所对应的名字作为目标的名字，记得前面加个“.”符号。
			 注意：可以用class来代替id选择器，并且class选择器还可以多次重用，可以更好的控制一个或多个标签。
			 * */
			.bg_black{
				background-color: black;
			}
		</style>
	</head>
	<body>
		<p class="bg_black" id="p1">今天是周一，天气棒棒哒</p>
		<p id="p2">我是p2</p>
		<p class="bg_black">我是p3</p>
	</body>
</html>
```