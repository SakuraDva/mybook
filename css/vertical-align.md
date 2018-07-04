#垂直方向的对齐方式

|属性|值|描述|
|:-  |:-|:- |
|vertical-align|top,middle,bottom|来控制行内块元素的上，中，下对齐|



#注意事项
1. 只针对行内块元素
	
2. 如果默认不设置，则对齐方式为baseline，也就是以最后一行的英文的基线为标准，进行垂直方向的对齐
	
3. 实际布局中，我们应该有意识的去设置vertical-align为top、middle或bottom，来更好的对齐我们的行内块元素。

##整体案例
```
<head>
		<meta charset="UTF-8">
		<title></title>
		<style type="text/css">
			*{
				margin: 0;
			}
			/**
			 * vertical-align  垂直方向的对齐方式
			 * 注意：1. 只针对行内块元素
			 * 		2. 如果默认不设置，则对齐方式为baseline，也就是以最后一行的英文的基线为标准，进行垂直方向的对齐
			 * 		3. 实际布局中，我们应该有意识的去设置vertical-align为top、middle或bottom，来更好的对齐我们的行内块元素。
			 */
			input{
				display: inline-block;
				/*vertical-align:middle ;*/
			}
			div{
				display: inline-block;
				height: 50px;
				width: 100px;
				background: red;
				/*vertical-align:middle ;*/
			}
		</style>
	</head>
	<body>
		<input type="text" />
		<input type="text" />
		<div>
			哈哈heihei
		</div>
	</body>
```