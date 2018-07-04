#固定定位position:fixed

与absolute一致，但偏移定位是以窗口为参考。当出现滚动条时，对象不会随着滚动。

#固定定位的特点
1.永远参照窗口的左上角作为基准点，不受任何父元素的控制。
	
2.通常可以用来固定某些元素在我们浏览器的窗口上。

#图片展示
<img src="../../media/fixed.png" />
#具体案例
```
	<head>
		<meta charset="UTF-8">
		<title></title>
		<style type="text/css">
			.ad{
				/*
				 fixed
				 1.永远参照窗口的左上角作为基准点，不受任何父元素的控制。
				 2.通常可以用来固定某些元素在我们浏览器的窗口上。
				 * */
				position: fixed;
				right: 0;
				bottom: 0;
			}
		</style>
	</head>
	<body>
		<div class="ad">
			我是一张小广告
			<img src="img/ad.png" />
		</div>
	</body>
```