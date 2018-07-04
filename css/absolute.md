#绝对定位position:absolute

把元素脱离文档流，通过left,right,top,bottom进行定位，参考点事body的最左上角。

#绝对定位的特点 
1.脱离文档流，所以不再占有正常文档流的位置
	
2.非常的自由，可以随意方便的设置位置信息，通常选择四个方向的2个就可以了。
	
3.不容易受控，不受元素结构的影响，也不受出生位置的影响，如果父元素不是带有定位信息，则根据body的左上角作为参考点。否则，则以父元素的左上角作为参考点。（带有定位信息的元素，是指设置了绝对定位，相对定位，固定定位的元素,但我们更推荐使用相对定位来管理绝对定位的元素）
				 

#图片展示
<img src="../../media/absolute.png" />
#具体案例 
```
	<head>
		<meta charset="utf-8" />
		<title></title>
		<style type="text/css">
			
			.test{
				width: 100px;
				height: 100px;
				background: skyblue;
				/*
				 绝对定位
				 把元素脱离文档流，通过left,right,top,bottom进行定位，参考点事body的最左上角。
				 1.脱离文档流，所以不再占有正常文档流的位置
				 2.非常的自由，可以随意方便的设置位置信息，通常选择四个方向的2个就可以了。
				 3.不容易受控，不受元素结构的影响，也不受出生位置的影响，如果父元素不是带有定位信息，则根据body的左上角作为参考点。否则，则以父元素的左上角作为参考点。（带有定位信息的元素，是指设置了绝对定位，相对定位，固定定位的元素,但我们更推荐使用相对定位来管理绝对定位的元素）
				 
				 * */
				position: absolute; /*设置定位信息为绝对定位*/
				left:100px ; /*距离左边100px*/
				/*right: ;*/
				top:100px ; /*距离顶部100px*/
				/*bottom: ;*/
			}
			.test2{
				width: 100px;
				height: 100px;
				background: pink;
			}
			.baba{
				width: 200px;
				height: 200px;
				background: black;
			}
		</style>
	</head>
	<body>
		<div class="test">
			我是一匹快乐的小灰狼
		</div>
		<div class="test2">
			我是一只柔弱的小肥羊
		</div>
	</body>
```