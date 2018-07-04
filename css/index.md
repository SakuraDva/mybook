#网页制作的流程

###顺序
1.先看设计图，思考如何布局，可以用笔纸或其他工具，把结构先大致画出来<br/>
2.思考使用什么样的元素标签，可以用最精简的结构来表达<br/>
3.先布局，先做大的，再做精细的，小的元素<br/>
4.制作过程当中，时刻留意盒子模型，利用浏览器的F12，或加背景颜色，去观察出来的效果是否有偏差，如果一发现有偏差，应该及时解决当前问题，再继续做下去。

###具体案例
<img src="../../media/index.png" />
```
<!DOCTYPE html>
<html>
	<head>
		<meta charset="UTF-8">
		<title></title>
		<style type="text/css">
			/*
			 1.先看设计图，思考如何布局，可以用笔纸或其他工具，把结构先大致画出来
			 2.思考使用什么样的元素标签，可以用最精简的结构来表达
			 3.先布局，先做大的，再做精细的，小的元素
			 4.制作过程当中，时刻留意盒子模型，利用浏览器的F12，或加背景颜色，去观察出来的效果是否有偏差，如果一发现有偏差，应该及时解决当前问题，再继续做下去。
			 * */
		    *{
		    	margin: 0;
		    	padding: 0;
		    }
		    .web{
		    	width: 800px;
		    	background: lightyellow;
		    	margin: 0 auto;/*宽度小于当前父元素的块级元素的水平居中*/
		    	list-style: none;/*去除列表的排序序号*/
		    	font-size: 0;
		    	padding: 35px 28px;
		    	box-sizing: border-box;/*改变盒子的模型，让width和height直接控制内容和内边距的区域*/
		    }
		    .web li{
		    	display: inline-block;
		    	text-align: center;
		    	font-size: 14px;
		    	margin-right: 34px;
		    	margin-bottom: 30px;
		    }
		    .web li img{
		    	width: 83px;
		    	height: 83px;
		    	border: 2px solid #258df2;
		    	border-radius:10px 0 10px 0 ;/*设置圆角边框*/
		    }
		    .web li h2{
		    	color:#363636;
		    	font-weight: normal;
		    	
		    }
		    .web li a{
		    	text-decoration: none;																
		    }
		    
		</style>
	</head>
	<body>
		<ul class="web">
			<li>
				<a href="">
					<img src="img/1.jpg"/>
					<h2>明世隐</h2>
				</a>
			</li>
			<li>
				<a href="">
					<img src="img/2.jpg"/>
					<h2>女娲</h2>
				</a>
			</li>
			<li>
				<a href="">
					<img src="img/3.jpg"/>
					<h2>梦奇</h2>
				</a>
			</li>
			<li>
				<a href="">
					<img src="img/4.jpg"/>
					<h2>苏烈</h2>
				</a>
			</li>
			<li>
				<a href="">
					<img src="img/5.jpg"/>
					<h2>百里玄策</h2>
				</a>
			</li>
			<li>
				<a href="">
					<img src="img/6.jpg"/>
					<h2>百里守约</h2>
				</a>
			</li>
			<li>
				<a href="">
					<img src="img/6.jpg"/>
					<h2>百里守约</h2>
				</a>
			</li>
			<li>
				<a href="">
					<img src="img/6.jpg"/>
					<h2>百里守约</h2>
				</a>
			</li>
			<li>
				<a href="">
					<img src="img/6.jpg"/>
					<h2>百里守约</h2>
				</a>
			</li><li>
				<a href="">
					<img src="img/6.jpg"/>
					<h2>百里守约</h2>
				</a>
			</li><li>
				<a href="">
					<img src="img/6.jpg"/>
					<h2>百里守约</h2>
				</a>
			</li><li>
				<a href="">
					<img src="img/6.jpg"/>
					<h2>百里守约</h2>
				</a>
			</li>
		</ul>
	</body>
</html>

```