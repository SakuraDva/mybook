#热区功能

|属性|说明|
|:-  |:-  |
|shape|定义区域的形状。(矩形rect，圆形circle，多边形poly)|
|coords|坐标值(定义可点击区域（对鼠标敏感的区域）的坐标。)|
|href|URL(定义此区域的目标URL地址)|
|target|点击过后如何在浏览器打开(_blank(在新的页面打开),_parent,_self,_top(在本页面打开)|

#关于map标签：
        定义一个客户端图像映射。图像映射（image-map）指带有可点击区域的一幅图像。
        注释：area 元素永远嵌套在 map 元素内部。area 元素可定义图像映射中的区域。
        注释：<img>中的 usemap 属性可引用 <map> 中的 id 或 name 属性（取决于浏览器），所以我们应同时向 <map> 添加 id 和 name 属性。
|属性|值|描述|
|:-  |:-  |
|(必须属性)id|unique_name|为map标签定义唯一的名称|
|(可选属性)name|mapname|为image-map规定名称|

```
<img src="img/map.jpg" alt="" usemap="#hotmap"/>
<map name="hotmap">
	<area shape="rect" coords="180,120,280,204" href="img标签.html"/>
	<area shape="circle" coords="641,95,60" href="a标签.html"/>
	<area shape="poly" coords="350,12,280,95,421,95" href="a锚点锚点.html"/>
</map>
```
#例子
<img src="../../media/map.jpg" alt="" usemap="#hotmap"/>
<map name="hotmap">
	<area shape="rect" coords="180,120,280,204" href="../../media/1.jpg" target="_blank">
	<area shape="circle" coords="641,95,60" href="../../media/2.jpg" target="_parent"/>
	<area shape="poly" coords="350,12,280,95,421,95" href="../../media/3.jpg" target="_top"/>
</map>
#心得
1.在网页上的一个区域的超链接<br/>
2.它是跟图片结合一起用的，可以把链接绑在图片的区域上，然后点击图片可以跳到跟图片的相关信息<br/>
3.定义图片的热区的时候用到