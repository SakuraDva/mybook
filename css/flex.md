#弹性盒子运用

##基础知识和专业术语
采用Flex布局的元素，称为Flex容器（flex container），简称"容器"。它的所有子元素自动成为容器成员，称为Flex项目（flex item），简称"项目"。<br/>
弹性盒子的核心概念:<br/>
<img src="../../media/flexbox.png" />
基本上，Flex项目是沿着main axis(从main-start向main-end)或者cross axis(从cross-start向cross-end)排列。<br/>
+ main axis:Flex容器的主轴主要用来配置Flex项目。注意，它不一定是水平，这主要取决于flex-direction属性。
+ main-start | main-end:Flex项目的配置从容器的主轴起点边开始，往主轴终点边结束。
+ main size:Flex项目的在主轴方向的宽度或高度就是项目的主轴长度，Flex项目的主轴长度属性是width或height属性，由哪一个对着主轴方向决定。
+ cross axis:与主轴垂直的轴称作侧轴，是侧轴方向的延伸。
+ cross-start | cross-end:伸缩行的配置从容器的侧轴起点边开始，往侧轴终点边结束。
+ cross size:Flex项目的在侧轴方向的宽度或高度就是项目的侧轴长度，Flex项目的侧轴长度属性是width或height属性，由哪一个对着侧轴方向决定。

##传统的布局方式
+ 浮动布局(float formattin Context ffc)
+ 行内块布局（inline-block formatting context ifc）
+ css3提出一种新的布局方案
+ 弹性盒子（ffc flex formatting context）
+ 规定：给父元素设置display为flex时，子元素vertical-align，float，clear都会失效。

---
##开启Flex容器：让一个元素变成伸缩容器 —— display
定义一个Flex容器，根据其取的值来决定是内联还是块。Flex容器会为其内容建立新的伸缩格式化上下文。
<img src="../../media/display-flex.png" />
```
.container {
  display: -webkit-flex; /* 兼容webkit内核浏览器*/
  display: flex; /* 也可以为行内元素设置 inline-flex */
}
```
###注意
1. CSS3的Columns属性对弹性容器是没有影响的（注：CSS3的Columns属性可以参见这里)
2. float, clear 和 vertical-align 对弹性块里的项目块没有影响。
3. 如果元素display的值指定为inline-flex，而且元素是一个浮动元素或绝对定位元素，则display的计算值是flex。

|规范版本|属性名称|块伸缩容器|行内块伸缩容器|
|:-    |:-    | :-     |:-       |
|标准版本(12版)|display|flex|inline-flex|
|混合版本(11版)|display|flexbox|inline-flexbox|
|最老版本(09版)|display|box|inline-box|

> 如果看到了display:box;或者“box-{*}属性，那么就是2009年版本的Flexbox。<br/>
> 如果看到了display:flexbox;或者“flex()函数，那么就是2011年版本的Flexbox。<br/>
> 如果你看到了display:flex;和flex-{*},那么就是2012版的Flexbox。<br/>
> 本文将以display:flex;书写。<br/>

---

##伸缩流：指定伸缩容器主轴的伸缩流方向 —— flex-direction(就是项目的排列顺序)
<img src="../../media/flex-direction.png"/>
这是用来创建方轴，从而定义Flex项目在Flex容器中放置的方向。Flexbox是一种单方向的布局概念。认为Flex项目主要排列方式要么是水平排列，要么是垂直列排列。
```
.container {
  flex-direction: row | row-reverse | column | column-reverse;
}
```
+ row(默认值):主轴为水平方向，起点在左端。(常规的文档流，从左往右,一行排列)
+ row-reverse:主轴为水平方向，起点在右端。(从右到左排列)
+ column:主轴为垂直方向，起点在上沿。(由上往下，进行排列)
+ column-reverse:主轴为垂直方向，起点在下沿。（由下往上，进行排列）

|规范版本|属性名称|水平方向|反向水平|垂直水平	|反向垂直|
|:-    |:-    |:-    |:-    |:-     |:-    |
|标准版本(12版)|flex-direciton|row|row-reverse|column|column-reverse|
|混合版本(11版)|flex-direction|row|row-reverse|column|column-reverse|
|最老版本(09版)|box-orient|horizontal|horizontal|vertical|	vertical|
|要设置两个属性|box-direction|normal|reverse|normal|reverse|



---


##换行：指定伸缩项目是否沿着侧轴排列 —— flex-wrap(项目是否换行)
<img src="../../media/flex-wrap.png"/>
默认情况之下，Flex项目都尽可能在一行显示。你可以根据flex-wrap的属性值来改变，让Flex项目多行显示。方向在这也扮演了一个重要角度，决定新的一行堆放方向。
```
.container{
    flex-wrap: nowrap | wrap | wrap-reverse;
}
```

+ nowrap(默认值):单行显示,绝不换行
+ wrap:多行显示，支持换行
+ wrap-reverse:多行显示，第一行在下方

|规范版本|属性名称|不换行|换行|反转换行|
|:-    |:-    |:-   |:- |:-    |
|标准版本(12版)|flex-wrap|nowrap|wrap|wrap-reverse|
|混合版本(11版)|flex-wrap|nowrap|wrap|wrap-reverse|
|最老版本(09版)|box-lines|single|multiple|N/A|

---


#主轴对齐方式 —— justify-content(项目水平方向对齐)
定义了项目在主轴上的对齐方式。
```
.container {
  justify-content: flex-start | flex-end | center | space-between | space-around;
}
```

<img src="../../media/justify-content.png"/>
+ flex-start(默认值):左对齐
+ flex-end:右对齐
+ center:居中对齐
+ space-between:两端对齐，项目之间的间隔都相等。
+ space-around:每个项目两侧的间隔相等。所以，项目之间的间隔比项目与边框的间隔大一倍。(平均分配多余空间)

|规范版本|属性名称|start|center|end|justify|distribute|
|:-    |:-    |:-   |:-    |:- |:-      |:-     |
|标准版本(12版)|justify-content|flex-start|center|flex-end|space-between|space-around|
|混合版本(11版)|flex-pack|start|center|end|justify|distribute|
|最老版本(09版)|flex-pack|start|center|end|justify|N/A|

---

#侧轴对齐方式 —— align-items(项目的垂直方向对齐)
定义项目在交叉轴上如何对齐
```
.container {
  align-items: flex-start | flex-end | center | baseline | stretch;
}
```

<img src="../../media/align-items.png"/>
###下面假设侧轴从上到下:
+ flex-start:侧轴起点对齐(顶部对齐)
+ flex-end:侧轴终点对齐（底部对齐）
+ center:侧轴居中对齐（垂直居中）
+ baseline:项目的第一行文字的基线对齐。(容器的基线上)
+ stretch(默认值):如果项目未设置高度或设为auto，将占满整个容器的高度。(注意:如果设置了min/max-width/height等属性的前提下,会尽可能接近所设置的尺寸。)（拉伸至填满容器）<br/>
注意：父容器的高度不能由内容撑起

|规范版本|属性名称|start|center|end|baseline|stretch|
|:-    |:-    |:-   |:-    |:- |:-      |:-     |
|标准版本(12版)|align-items|flex-start|center|flex-end|baseline|stretch|
|混合版本(11版)|flex-align|start|center|end|baseline|stretch|
|最老版本(09版)|box-align|start|center|end|baseline|stretch|


---

#定义flex子项单独在侧轴（纵轴）方向上的对齐方式。-align-self(控制单一项目的垂直方向对齐方式)
<img src="../../media/align-self.png"/>
<img src="../../media/align-self1.png"/>

###下面假设侧轴从上到下:
+ auto：如果'align-self'的值为'auto'，则其计算值为元素的父元素的'align-items'值，如果其没有父元素，则计算值为'stretch'。
+ flex-start：弹性盒子元素的侧轴（纵轴）起始位置的边界紧靠住该行的侧轴起始边界。(顶部对齐)
+ flex-end：弹性盒子元素的侧轴（纵轴）起始位置的边界紧靠住该行的侧轴结束边界。（底部对齐）
+ center：弹性盒子元素在该行的侧轴（纵轴）上居中放置。（如果该行的尺寸小于弹性盒子元素的尺寸，则会向两个方向溢出相同的长度）。（垂直居中）
+ baseline：如弹性盒子元素的行内轴与侧轴为同一条，则该值与'flex-start'等效。其它情况下，该值将参与基线对齐。(容器的基线上)
+ stretch：如果指定侧轴大小的属性值为'auto'，则其值会使项目的边距盒的尺寸尽可能接近所在行的尺寸，但同时会遵照'min/max-width/height'属性的限制。（填满整个容器）

|规范版本|属性名称|start|center|end|baseline|stretch|
|:-    |:-    |:-   |:-    |:- |:-      |:-     |



---

#伸缩项目行对齐方式 —— align-content(控制多个轴的项目的垂直对齐方式)
当伸缩容器的侧轴还有多余空间时，`align-content`属性可以用来调准伸缩行在伸缩容器里的对齐方式，这与调准伸缩项目在主轴上对齐方式的`justify-content`属性类似。

```
.test {
  align-content: flex-start(顶部对齐) | flex-end （底部对齐）| center （垂直居中）| space-between(容器的基线上) | space-around | stretch （填满整个容器）;
}
```
<img src="../../media/align-content.png" />

+ flex-start:与侧轴的起点对齐 (从最左边对齐)
+ flex-end:与侧轴的终点对齐。(从最右边对齐)
+ center:与侧轴的中点对齐。  （侧轴的垂直居中对齐）
+ space-between:与侧轴两端对齐，轴线之间的间隔平均分布。 （填满整个容器）
+ space-around:每根轴线两侧的间隔都相等。所以，轴线之间的间隔比轴线与边框的间隔大一倍。。
+ stretch(默认值):轴线占满整个交叉轴。

###注意
1. 这个属性当只有一行伸缩容器的时候是没有效果的。
2. 只有多行的伸缩容器的时候才会在侧轴有多余的空间才会进行对齐



|规范版本|属性名称|start|center|end|justify|distribute|stretch|



#具体案例
```
<html>
	<head>
		<meta charset="utf-8" />
		<title>flex弹性盒子</title>
		<style type="text/css">
			*{
				margin: 0;
				padding: 0;
			}
			.baba{
				/*将容器转换为弹性盒子*/
				display: flex;
				width: 800px;
				height: 300px;
				/*display: inline-flex;*/
				background: skyblue;
				/*项目的排列方式
				 默认值：row(常规的文档流，从左往右,一行排列)
				        row-reverse(从右到左排列)
				        column(由上往下，进行排列)
				        column-reverse（由下往上，进行排列）
				 * */
				flex-direction: row;
				/*
				 项目是否换行
				 默认值：nowrap不换行
				        wrap换行
				 * */
				flex-wrap: nowrap;
				/*
				 排列方式是否换行的综合写法
				 * */
				flex-flow: row nowrap; (默认值)
			}
			.baba p{
				background: red;
			}
			/*
			 项目的排列顺序
			 order 默认值为0，支持（正负数）整数
			 
			 * */
			.baba p:last-child{
				order: 0;
			}
			
			
			/*第二部分：项目的对齐方式
			   项目水平方向
			   spaace-between 两端对齐
			   space-around  平均分配多余空间
			   flex-start   左对齐
			   flex-end   右对齐	
			   center    居中对齐
			   
			   项目垂直方向对齐方式
			   align-ierms
			   flex-start (顶部对齐)
			   flex-end （底部对齐）
			   flex-center （垂直居中）
			   flex-baseline   (容器的基线上)
			   flex-stretch  （拉伸至填满容器）
			   注意：父容器的高度不能由内容撑起
			 * */
			.baba{
				justify-content: space-around;
				align-items: stretch;
			}
			/*
			  控制单一项目的垂直方向对齐方式
			   align-ierms
			   flex-start (顶部对齐)
			   flex-end （底部对齐）
			   flex-center （垂直居中）
			   flex-baseline   (容器的基线上)
			   flex-stretch  （填满整个容器）
			 * */
			.baba p:first-child{
				align-self: flex-end;
			}
			
			/*
			 align-content   控制多个轴，项目的垂直对齐方式
			   flex-start (顶部对齐)
			   flex-end （底部对齐）
			   flex-center （垂直居中）
			   flex-baseline   (容器的基线上)
			   flex-stretch  （填满整个容器）
			 * */
			.baba{
				/*width: 400px;
				flex-wrap: wrap;
				align-content: space-between;*/
			}
			
			
			/*第三部分   
			   项目的伸缩
			 * 
			 * 项目的放大属性
			 * flex-grow    放大因子 默认值为0
			 * flex-shrink
			 * 
			 * 
			 * */
			.baba p:first-child{
				/*flex-grow: 1;*/
				/*放大因子*/
			}
			.baba p:nth-child(2){
				/*flex-grow: 1;*/
			}
			.baba p:last-child{
				/*flex-grow: 1;*/
			}
			/*项目缩小属性
			 flex-shrink    默认值为1
			 * */
			.baba p:first-child{
				/*flex-shrink: 1;*/
			}
			.baba p:nth-child(2){
				/*flex-shrink: 1;*/
			}
			.baba p:last-child{
				/*flex-shrink: 1;*/
			}
			/*
			 flex-basis   容器分配之前，项目先占的空间
			 * */
			.baba p:first-child{
				flex-basis: 200px;
			}
			
			/*弹性盒子的综合写法*/
			.baba p:first-child{
				flex:0 1 auto;
			/*(默认值：放大因子,缩小因子,先占空间)*/
			}
		</style>
	</head>
	<body>
		<!--
			传统高布局方式
			浮动布局(float formattin Context ffc)
			行内块布局（inline-block formatting context ifc）
			css3提出一种新的布局方案
			弹性盒子（ffc flex formatting context）
			规定：给父元素设置display为flex时，子元素vertical-align，float，clear都会失效。
			
		-->
		<div class="baba">
			<p>我是爸爸里面的儿子1</p>
			<p>我是爸爸里面的儿子2</p>
			<p>我是爸爸里面的儿子3</p>
		</div>
	</body>
</html>
```


























