#Color颜色属性


###颜色的取值，分三种
1.单词模式    （优点容易记忆，缺点颜色精准性较差）
    
    background-color="skyblue";
    
2.16进制模式  （#00ff22  十六进制： 0-9 和 a-f ）
    
    background-color: #ff0000;
    
3.rgba模式    RGB+Alpha透明度  （RGB取值范围是0-255，A取值范围是0-1）
    
    background-color: rgba(255,0,0,.5);
    
4.hsla模式    (h  0-360代表颜色 ,  s  0.0%-100.0%代表灰度 ,l  0.0%-100.0%代表亮度   )
    
    background-color: hsla(0,100%,54%,1);
    

#注意
第四种在css中不是经常使用，而用在3D上

#颜色分配图
<img src="../../media/color.jpg" />

```
<html>
<head>
	<meta charset="UTF-8">
	<title>颜色</title>
	<style type="text/css">
		.test{
			height: 300px;
			/*
			 颜色的取值，分三种
			 1.单词模式    （优点容易记忆，缺点颜色精准性较差）
			 2.16进制模式  （#00ff22  十六进制： 0-9 和 a-f ）
			 3.rgba模式    RGB+Alpha透明度  （RGB取值范围是0-255，A取值范围是0-1）
			 4.hsla模式    (h  0-360代表颜色 ,  s  0.0%-100.0%代表灰度 ,l  0.0%-100.0%代表亮度   )
			 * */
			/*background-color: #ff0000;*/
			/*半透明红色*/
			/*background-color: rgba(255,0,0,.5);*/
			background-color: hsla(0,100%,54%,1);
		}
	</style>
</head>
<body>
	<div class="test">
		啦啦啦还是我
	</div>
</body>
</html>
```