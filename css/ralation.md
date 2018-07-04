#关系选择器


 
#关系选择器中-父子关系（>）
通过制定父元素以及其具体的子元素，来制定我们的控制目标
    
注意：更精确的控制，可以小范围的控制某一类元素。
```
.nav > li{
	font-size: 30px;
	font-weight: bold;
}
<body>
 <ul class="nav">
 	<li>首页</li>
 	<li>产品
 	<ul class="subnav">
 		<li class="egg">鸡蛋</li>
 		<li>鹅蛋</li>
 		<li>炸弹</li>
 		<li>恐龙蛋</li>
 	</ul>
 	</li>
 	<li>关于我们</li>
 </ul>
</body>
```

#关系选择器中-后代关系（空格）
通过写出父元素及其后代元素，来指定为我们的控制目标
    
注意：这种会比父子元素，控制的范围要大，因为他是针对所有的后代元素。
```
.nav li{
	text-shadow: 2px 2px 5px gray /*字体阴影*/;
}
<body>
 <ul class="nav">
 	<li>首页</li>
 	<li>产品
 	<ul class="subnav">
 		<li class="egg">鸡蛋</li>
 		<li>鹅蛋</li>
 		<li>炸弹</li>
 		<li>恐龙蛋</li>
 	</ul>
 	</li>
 	<li>关于我们</li>
 </ul>
</body>
```
#关系选择器中-相邻关系（+）
通过写出参照元素和它的相邻元素，来指定为我们的控制的目标
    
注意：控制的是其中一个兄弟元素
```
.subnav>li+li{
		color: blue;
	}
		<body>
 <ul class="nav">
 	<li>首页</li>
 	<li>产品
	 	<ul class="subnav">
	 		<li class="egg">鸡蛋</li>
	 		<li>鹅蛋</li>
	 		<li>炸弹</li>
	 		<li>恐龙蛋</li>
	 	</ul>
 	</li>
 	<li>关于我们</li>
 </ul>
</body>
```
#关系选择器中-兄弟关系（~）
通过写出参照元素和它的后续同辈元素，来指定为我们的控制目标
    
注意：控住的是后续的所有符合条件的兄弟元素
```
.egg~li{
			border: 10px solid pink;
		}
		 <ul class="nav">
<li>首页</li>
<li>产品
 	<ul class="subnav">
 		<li class="egg">鸡蛋</li>
 		<li>鹅蛋</li>
 		<li>炸弹</li>
 		<li>恐龙蛋</li>
 	</ul>
 	</li>
 	<li>关于我们</li>
 </ul>
</body>
```

更多信息:http://www.css88.com/book/css/selectors/relationship/index.htm