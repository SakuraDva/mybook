#浮动

|属性|值|描述|
|:-  |:-|:-  |
|float|none|设置对象不浮动|
|float|left|设置对象左浮动|
|float|right|设置对象右浮动|

#说明
1.不管元素是什么类型，都会具有这种浮动能力，并且不会像行内块那样有空隙，元素之间是紧密排列的。
	
2.但也会脱离了文档流，也就是不再跟普通的非浮动元素待在同一个空间，所以，可能会出现重叠的现象。
	
3.所以，我们会用清除浮动，来抵消刚刚的第二点所带来的副作用。（也就是还原浮动元素本该占有的面积）



#清除浮动,最常见的3种方式
1.直接给浮动元素的爸爸加高度。（不推荐使用，因为比较死板）
	
2.直接跟在连续浮动元素的后面，追加一个块级元素，并设置为clear:both（推荐使用，也相对灵活）
	```
	 浮动
	 浮动
		
	 非浮动
	 浮动
		
	 非浮动
	 以上实例可以看到，有两处是需要添加清除浮动。
	```
	
3.控制浮动元素的爸爸after选择器，设置为块级元素和clear:both。（推荐使用，但仅限于某一组浮动元素来使用，如果是浮动元素和非浮动元素掺杂在一起，较为复杂的话，此方法不适用）
	```
		.clear{
			clear: both;
		}
		.clearfix::after{
			content: "";
			display: block;
			clear: both;
		}
	```


##具体案例
```
<head>
		<meta charset="UTF-8">
		<title></title>
		<style type="text/css">
			/*
			 浮动
			 1.不管元素是什么类型，都会具有这种浮动能力，并且不会像行内块那样有空隙，元素之间是紧密排列的。
			 2.但也会脱离了文档流，也就是不再跟普通的非浮动元素待在同一个空间，所以，可能会出现重叠的现象。
			 3.所以，我们会用清除浮动，来抵消刚刚的第二点所带来的副作用。（也就是还原浮动元素本该占有的面积）
			 * */
			div,p,a,span{
				float: left;
			}
			.pingmin{
				height: 300px;
				background: skyblue;
				float: none;
			}
			.clear{
				float: none;
				clear: both;
				text-align: center;
				background: pink;
			}
		</style>
	</head>
	<body>
		<div>
			我是一个div
		</div>
		<p>
			我是一个P
		</p>
		<a href="">我是一个a</a>
		<span>我是一个span</span>
		<div class="clear">我是一条清除线，呵呵，我可以把上面的浮动元素的兄弟，保护起来，不会被下面的非浮动元素侵占</div>
		<div class="pingmin">
			我是一个无辜的平民
		</div>
	</body>
	</body>
```