#文字的处理

#文档流  
1.根据浏览器的默认渲染顺序，从上往下，从左往右依次排列。
	
2.只要是按照正常文档流排序的元素，它的占地面积，是根据盒子模型计算而来。



#white-space   文字换行的处理机制
|属性|值|描述|
|:-  |:-|:-  |
|white-space|normal|默认值，文字遇到容器边缘位置，会自动换行|
|white-space|nowrap|禁止换行，文字遇到容器边缘位置，强制不换行|
|white-space|pre|禁止换行，并且把容器内的所有空格和换行，一字不漏的显示出来|
|white-space|pre-wrap|用等宽字体显示预先格式化的文本，不合并文字间的空白距离，当文字碰到边界时发生换行。|
|white-space|pre-line|保持文本的换行，不保留文字间的空白距离，当文字碰到边界时发生换行。|


#单行溢出处理
1.white-space: nowrap;/*强制单行输出，防止文字跑到下一行，而没触发边界*/
	
2.overflow: hidden;/*创建边界，超出边界隐藏内容*/
	
3.text-overflow: ellipsis;/*文字遇到边界时，显示省略号*/


#多行溢出处理
注意：文字的容器的高度，必须刚好是行高乘与最大支持行数
	
文字的容器的高度   =  行高 * 最大支持行数
	
1.overflow:hidden ;/*1.超出内容要隐藏，创建边界*/
	
2.text-overflow: ellipsis;     /*2.文字遇到边界时，显示省略号*/
	
3.display: -webkit-box;        /*3.设置该容器为弹性盒子*/
	
4.-webkit-line-clamp: 2;       /*4.表示你的文字可以支持的最大行数*/
	
5.-webkit-box-orient: vertical;/*5.设置文字排版方向从上到下*/
	
##图片案例
<img src="../../media/textdispose.png" />


#针对图片的布局
1. 给图片添加一个外围容器，用来限制图片的显示区域
	
2. 可以根据实际情况，选择宽自适应（图片宽设为100%）或高自适应（图片的高设为100%）
	 ```
	 .web > li div{
		width: 83px;
		height: 83px;
		border: 2px solid #258df2;
		border-radius: 10px 0 10px 0;
		overflow: hidden;
	}
	.fixWidth{
		vertical-align: middle;
	}
	.fixWidth>img{
		width: 100%;
	}
	.fixHeight{
		text-align: center;
	}
	.fixHeight>img{
		height: 100%;
	}
 ```


#具体案例
```
	<head>
		<meta charset="UTF-8">
		<title></title>
		<style type="text/css">
			div{
				width: 200px;
				height: 50px;
				line-height: 20px;
				background: skyblue;
				/*
				 white-space   文字换行的处理机制
				 normal        默认值，文字遇到容器边缘位置，会自动换行
				 nowrap        禁止换行，文字遇到容器边缘位置，强制不换行
				 pre           禁止换行，并且把容器内的所有空格和换行，一字不漏的显示出来
				 
				 * */
				white-space: normal;
				/*white-space: nowrap; 
				white-space: pre;*/
				
				/*
				 单行溢出处理
				 * */
				white-space: nowrap;/*强制单行输出，防止文字跑到下一行，而没触发边界*/
				overflow: hidden;/*创建边界，超出边界隐藏内容*/
				text-overflow: ellipsis;/*文字遇到边界时，显示省略号*/
				
				
				
			}
			p{
				width: 200px;
				height:50px;
				line-height: 25px;
				/*
				 多行溢出处理
				 注意：文字的容器的高度，必须刚好是行高乘与最大支持行数
				     文字的容器的高度   =  行高 * 最大支持行数
				 * */
				overflow:hidden ;            /*1.超出内容要隐藏，创建边界*/
				text-overflow: ellipsis;     /*2.文字遇到边界时，显示省略号*/
				display: -webkit-box;        /*3.设置该容器为弹性盒子*/
				-webkit-line-clamp: 2;       /*4.表示你的文字可以支持的最大行数*/
				-webkit-box-orient: vertical;/*5.设置文字排版方向从上到下*/
				
				
			}
		</style>
	</head>
	<body>
		<div>
			我是一件商品，我的名字很长，长到你看不完。你真的是看不完的拉啦啦啦啊
		</div>
	   <p>
	   	我是一件商品，我的名字很长，长到你看不完。你真的是看不完的拉啦啦啦啊
	   </p>
	</body>
```
#心得
