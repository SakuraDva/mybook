#Font属性

|属性|值|描述|
|:-  |:-|:- |
|font-size|px,%|控制字体的大小(用百分比的时候，是基于父对象的字体大小进行百分比计算)|
|font-weight|normal,bold,bolder,lighter|字体的粗细，通常加粗就写bold，不加粗就写normal|
|font-style|normal,italic,oblique|字体的倾斜，通常斜体就写italic，不需要就写normal|
|font-variant|normal,small-caps|小型的大写字母，只能用在内容中的小写字母，使用频率不高|
|font-family|name,generic|设置或检索用于对象中文本的字体名称序列。|

#网站字体:只分为衬线和非衬线
通常网站主流使用非衬线字体(sans serif)

|系统|英文|中文|
|:-  |:-  |:- |
|win|Arial |Microsoft  YaHei|
|mac|Helvetica neue,Helvetica|PingFang SC,Hiragino Sans GB,Heiti SC| 

##写法上：
1.优先写mac系统，再写win系统，优先写英文字体，再写中文字体
    
2.在浏览器应用过程中，会优先判断英文字体，再判断中文字体，多个字体要用逗号隔开，如果字体带有空格都需要用引号包起来,浏览器则按照先后顺序依次使用可用字体。
###例子
```
font-family:  "Helvetica Neue",Helvetica,Arial,"PingFang SC","Hiragino Sans GB","Heiti SC","sans-serif";
```
#整合写法
以上属性都是单独的写法，我们可以用font进行整合
    
实际使用，还是建议根据需求写独立属性，更容易记忆和理解。

###例子
```
font:italic bold small-caps 24px / 32px  "Helvetica Neue",Helvetica,Arial,
				"PingFang SC","Hiragino Sans GB","Heiti SC","sans-serif";
```
#案列
```
<style type="text/css">
/*style可以写到任意的地方*/
body{
	font-size: 30px;
}
.test{
	/*控制字体的大小*/
	font-size: 24px; 
	font-size: 200%;/*除了绝对值，也可以用百分比，基于父对象的字体大小进行百分比计算*/
	font-weight: bold;/*字体的粗细，通常加粗就写bold，不加粗就写normal*/
	font-style: italic;/*字体的倾斜，通常斜体就写italic，不需要就写normal*/
	font-variant: small-caps;/*小型的大写字母，只能用在内容中的小写字母，使用频率不高*/
	
	
	/*
	 网站字体：只要分为衬线和非衬线
	 通常网站主流使用非衬线字体(sans serif)
	                   英文                                             中文
	 Win      | Arial                   |Microsoft  YaHei 
	 mac      | Helvetica neue,Helvetica| PingFang SC,Hiragino Sans GB,Heiti SC
	 写法上：优先写mac系统，再写win系统，优先写英文字体，再写中文字体       S
	 注意：在浏览器应用过程中，会优先判断英文字体，再判断中文字体，多个字体要用逗号隔开，如果字体带有空格都需要用引号包起来。
	 Helvetica neue,Helvetica,Arial,PingFang sc,Hiragino Sans GB,Heiti SC,"sans-serif"
	 * */
	font-family:  "Helvetica Neue",Helvetica,Arial,"PingFang SC","Hiragino Sans GB","Heiti SC","sans-serif";
	
	/*
	 以上属性都是单独的写法，我们可以用font进行整合
	 实际使用，还是建议根据需求写独立属性，更容易记忆和理解。
	 * */
	font:italic bold small-caps 24px / 32px  "Helvetica Neue",Helvetica,Arial,
	"PingFang SC","Hiragino Sans GB","Heiti SC","sans-serif"
}


</style>
</head>
<body>
<div class="test">
 我是一个div,2333
</div>
</body>
```