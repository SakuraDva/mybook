#伪对象选择器

#E：first-line:设置第一行样式
此伪对象仅作用于块对象。内联对象要使用该伪对象，必须先将其设置为块级对象。
    
IE6在使用该选择符时有个显式的BUG：选择符与包含规则的花括号之间不能紧挨着，需留有空格或换行。同时还存在该BUG的选择符包括：E:first-letter
    
CSS3将伪对象选择符(Pseudo-Element Selectors)前面的单个冒号(:)修改为双冒号(::)用以区别伪类选择符(Pseudo-Classes Selectors)，但以前的写法仍然有效。
    
即E:first-line可转化为E::first-line

```
p:first-line {color:#006600;}
p::first-line {color:#440000;}
    
    
    
<body>
<h1>第一行文字的颜色与其它不同</h1>
<p>今天，阳光明媚，晴空万里，非常适合户外活动，如踏青、远足之类的。长期坐在办公室的同学们要多注意运动。</p>
</body>
```
#E：first-letter:设置第一个字

```
p:first-line {color:#006600; font-size:50px;}
p::first-line {color:#440000; font-size:80px;}
	
	
    
<body>
<h1>杂志常用的首字下沉效果</h1>
<p>今天，阳光明媚，晴空万里，非常适合户外活动，如踏青、远足之类的。长期坐在办公室的同学们要多注意运动。</p><!--杂志常用的首字下沉效果-->
</body>
```

#E:before/E::before { sRules }（在XXX元素内容之前）
设置在对象前（依据对象树的逻辑结构）发生的内容。用来和content属性一起使用，并且必须定义content属性
    
CSS3将伪对象选择符(Pseudo-Element Selectors)前面的单个冒号(:)修改为双冒号(::)用以区别伪类选择符(Pseudo-Classes Selectors)，但以前的写法仍然有效。
    
即E:before可转化为E::before

#注意
1.本质上并不支持伪元素的双冒号(::)写法，而是忽略掉了其中的一个冒号，仍以单冒号来解析，所以等同变相支持了E::before。
    
2.不支持设置属性position, float, list-style-*和一些display值，Firefox3.5开始取消这些限制。
    
3.IE10在使用伪元素动画有一个问题：
```
<style>
p{position:relative;color:#f00;font-size:14px;font-size:0\9;*font-size:14px;}
p:before{position:absolute;background:#fff;color:#000;content:"如果你的能看到这段文字，说明你的浏览器只支持E:before";font-size:14px;}
p::before{position:absolute;background:#fff;color:#000;content:"如果你的能看到这段文字，说明你的浏览器支持E:before和E::before";font-size:14px;}
</style>
</head>
<body>
<p>Sorry, 你的浏览器不支持E:before和E::before</p>
</body>
```

#E:after/E::after { sRules }(在XXX元素内容之后)
设置在对象后（依据对象树的逻辑结构）发生的内容。用来和content属性一起使用，并且必须定义content属性
    
CSS3将伪对象选择符(Pseudo-Element Selectors)前面的单个冒号(:)修改为双冒号(::)用以区别伪类选择符(Pseudo-Classes Selectors)，但以前的写法仍然有效。
    
即E:after可转化为E::after
```
<style>
p{position:relative;color:#f00;font-size:14px;font-size:0\9;*font-size:14px;}
p:after{position:absolute;left:0;background:#fff;color:#000;content:"如果你的能看到这段文字，说明你的浏览器只支持E:after";font-size:14px;}
p::after{position:absolute;left:0;background:#fff;color:#000;content:"如果你的能看到这段文字，说明你的浏览器支持E:after和E::after";font-size:14px;}
</style>
</head>
<body>
<p>Sorry, 你的浏览器不支持E:after和E::after</p>
</body>
```
#E::selection { sRules }(设置元素被选中时的样式)
例子：
```
<style>
p::-moz-selection{background:#000;color:#f00;}
p::selection{background:#000;color:#f00;}
</style>
</head>
<body>
<h1>选中下面的文字，看看它的颜色</h1>
<p>你选中这段文字后，看看它们的文本颜色和背景色，就能明白::selection的作用。</p>
</body>
```
