#相对行为position:relative

通常用来控制绝对定位的元素

#相对定位的特点
1.并没有脱离文档流，相对定位是指相对于这个元素本身所在文档流的位置，进行偏移。（所以参考点是它自己本身的位置的左上角）。
	
2.正常使用过程中，我们通常不会使用left等值，去改变他的位置，因为这样不利于我们的布局。


#图片展示
<img src="../../media/relative.png" />

#具体案例
```
	<head>
		<meta charset="UTF-8">
		<title></title>
		<style type="text/css">
			.baba{
				width: 300px;
				height: 300px;
				background: black;
				/*
				 相对定位
				 通常用来控制绝对定位的元素
				 1.并没有脱离文档流，相对定位是指相对于这个元素本身所在文档流的位置，进行偏移。（所以参考点是它自己本身的位置的左上角）。
				 2.正常使用过程中，我们通常不会使用left等值，去改变他的位置，因为这样不利于我们的布局。
				 * */
				position: relative;
				left: 100px;
				top: 100px;
			}
			.son{
				width: 50px;
				height: 50px;
				background: red;
				position: absolute;
				left: 30px;
				top: 30px;
			}
		</style>
	</head>
	<body>
		<div class="baba">
			<div class="son">
				
			</div>
		</div>
	</body>
```