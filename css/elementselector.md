#Element Selector元素选择器

在 W3C 标准中，元素选择器又称为类型选择器（type selector）。

在 W3C 标准中，元素选择器又称为类型选择器（type selector）。

下面的规则匹配文档树中所有 h1 元素：
    h1 {font-family: sans-serif;}

```
<!DOCTYPE html>
<html>
	<head>
		<meta charset="UTF-8">
		<title></title>
		<style type="text/css">
			/*
			 元素选择器
			 以元素的名字，来作为目标名
			 注意：针对的是当前页面的所有p元素。
			 * */
			p{
				color: skyblue;
			}
		</style>
	</head>
	<body>
		<!--
			标签跟元素是一个意思
		-->
		<p>今天是周一，天气棒棒哒</p>
		<p>我是p2</p>	
	</body>
</html>
```