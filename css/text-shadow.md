#Text-shadow文本阴影属性
设置或检索对象中文本的文字是否有阴影及模糊效果。

|值|描述|
|:-|:- |
|color|设置对象的阴影的颜色。|
|length1|第1个长度值用来设置对象的阴影水平偏移值。可以为负值|
|length2|第2个长度值用来设置对象的阴影垂直偏移值。可以为负值|
|length3|如果提供了第3个长度值则用来设置对象的阴影模糊值。不允许负值|

#注意
可以设定多组效果，每组参数值以逗号分隔。多组阴影特殊效果
    
它拥有后期的动画性。

```
<html>
	<head>
		<meta charset="UTF-8">
		<title>阴影</title>
		<style type="text/css">
			div{
				text-shadow: 2px 2px gray,2px 2px ;
			}
		</style>
	</head>
	<body>
	      <div class="test">
	      	   准备要吃饭了
	      </div>
	</body>
</html>
```
更多详细:http://www.css88.com/book/css/properties/text-decoration/text-shadow.htm