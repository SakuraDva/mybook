#pseudoclass伪类选择器

在指定范围内的元素，精细控制其中某一个元素
    
注意：对现有的目标元素，进行更加详细的状态控制。
    
尽量不要这样子写，因为效率低。所以应该尽可能加上一个父元素，缩小搜索的范围

#child系列
.nav下的第一个li
.nav li:first-child
    
.nav下最后的一个li
.nav li:last-child
    
.nav下中间的那个li
.nav li:nth-child(2)

```
.nav li:first-child{
				color: skyblue;
}
.nav li:last-child{
   color: darkblue;
}
.nav li:nth-child(2){
	color: pink;
}
```
#type系列
根据指定元素的类型，来做精准控制
.nav的li类型下的最后一个li  
.nav li:last-of-type
    
.nav的li类型下的第一个li 
.nav li:first-of-type

.nav的li类型下的中间一个li 
.nav li:nth-of-type(2)

```
.nav li:last-of-type{
	color:pink;
}
.nav li:first-of-type{
	color:purple;
}
.nav li:nth-of-type(2){
	color:yellow;
}
```
#使用注意
1.如果子元素的类型不定，但位置相对固定，应该选择nth-child系列，粗暴直接，根据位置决定
    
2.如果子元素的类型相对固定且统一，应该选择nth-of-type系列，效率更高。
    
3.nth-child系列，首要条件是符合位置，然后才考虑指定的元素类型。
     
4.nth-of-type系列，首要满足必须是指定的元素类型，然后才考虑位置。

#针对超链接的伪类(hover和active适用于所有标签)
link：还没浏览链接
    
visited：准备浏览
    
active：点击链接
    
hover：鼠标移到链接

#注意
   1.通常制作中，我们用的更多的是hover
    
    2.没hover的时候，表示正常状态
     
     3.有hover的时候，表示激活状态（互动状态）
```
.nav a:link{
	background: skyblue;
}
.nav a:visited{
	background:green;
}
.nav a:hover{
	background: yellow;
}
.nav a:active{
	background: red;
}
```
#nth-child   nth-of-type  区别
```
ul li:first-of-type{  ul下面的第一个li类型的子元素
	background:purple;
}
ul :first-child{    ul下面的第一个子元素
  	background:skyblue;
   }
ul li:first-child{  ul下面的第一个子元素，并且是li类型，所以这里是不符合现有条件，是不会生效的
	background:skyblue
```