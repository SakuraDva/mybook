#ul列表
ul通常表示无序列表，信息的顺序是没有前后之分。

|属性|值|描述|
|:-|:-|:-|
|type|disc(实心圆),cirecle(空心圆),square(方形)|排序的符号|
|compact|compact(紧密的)|规定列表呈现的效果比正常情况更小巧。|

注意：ul标签里面正常只能容纳li
```
<ul type="square">
	<li>首页</li>
	<li>
		产品列表
	    <ul>
	    	<li>衣服</li>
	    	<li>袜子</li>
	    	<li>裤子</li>
	    </ul>
	</li>
	<li>新闻中心</li>
</ul>
```
#例子
<ul type="square">
	<li>首页</li>
	<li>
		产品列表
	    <ul>
	    	<li>衣服</li>
	    	<li>袜子</li>
	    	<li>裤子</li>
	    </ul>
	</li>
	<li>新闻中心</li>
</ul>