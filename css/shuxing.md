#属性选择器

#E[att] { sRules }:(只要具备指定属性可以选中)
```
input[type]{
				border: 10px solid black;
			}
```

#E[att="val"] { sRules }:(指定属性等于每个具体)

```
input[name="user"]{
				color: skyblue;
			}
```
#E[att~="val"] { sRules }:(选择具有att属性且属性值为一用空格分隔的字词列表，其中一个等于val的E元素（包含只有一个值且该值等于val的情况）。)
    
表示元素定义内只要有关于val的名字，则应用这样式。
```
<style>
a[class~="external"] {
	color: #f00;
}
</style>
</head>
<body>
<ul>
	<li><a href="?" class="external txt">外部链接</a></li>
	<li><a href="?" class="txt">内部链接</a></li>
	<li><a href="?" class="external txt">外部链接</a></li>
	<li><a href="?" class="txt">内部链接</a></li>
</ul>
</body>
</html>
```

#E[att^="val"] { sRules }:（选择具有att属性且属性值为以val开头的字符串的E元素。）
    
表示只要是元素定义内以Val开头的定义，则应用这样式。
```
<style>
div[class^="a"] {
	border: 2px solid #000;
}
</style>

<div class="abc">1</div>
<div class="acb">2</div>
<div class="bac">3</div>
```

#E[att$="val"] { sRules }:（选择具有att属性且属性值为以val结尾的字符串的E元素。）

则这个与上面相反，这个是以Val的结尾来使用样式。
```
<style>
li[class$="a"] {
	color: #f00;
}
</style>
</head>
<body>
<ul>
	<li class="abc">列表项目</li>
	<li class="acb">列表项目</li>
	<li class="bac">列表项目</li>
	<li class="bca">列表项目</li>
	<li class="cab">列表项目</li>
	<li class="cba">列表项目</li>
</ul>
</body>
</html>
```

#E[att*="val"] { sRules }:（指定属性只要包含关键字就符合要求）
    

```
input[class *="checkbox"]{
				backrgound:skyblue;
			}
```

#E[att|="val"] { sRules }:(以val开头，并且用-分割的属性，就符合要求)
    
#注意
选择具有att属性且属性值为以val开头并用连接符"-"分隔的字符串的E元素，如果属性值仅为val，也将被选择。
```
<style>
div[class|="a"] {
    border: 5px solid #666;
}
</style>
<!--1,3,4都会被选中-->
<div class="a-test">1</div>
<div class="b-test">2</div>
<div class="a-test"">3</div>
<div class="a">4</div>
```