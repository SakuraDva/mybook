#Text-decoration文本装饰线条
复合属性。检索或设置对象中的文本的装饰。


|值|描述|
|:-|:- |
|underline|在文本的底部添加下划线|
|line-through|在文本中间添加删除线|
|overline|在文本顶部添加顶部线|


```
<html>
	<head>
		<meta charset="UTF-8">
		<title></title>
		<style type="text/css">
			.test{
				text-decoration: underline;/*在文本的底部添加下划线*/
				text-decoration: line-through;/*在文本中间添加删除线*/
				text-decoration: overline;/*在文本顶部添加顶部线*/
				text-decoration: underline line-through overline;
			}
		</style>
	</head>
	<body>
		<div class="test">
			文本修饰属性
		</div>
	</body>
</html>
```
更多详细：http://www.css88.com/book/css/properties/text-decoration/text-decoration.htm