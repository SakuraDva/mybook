#Sass的快速入门
#1. 变量
```
sass中可以定义变量，方便统一修改和维护。
```
sass代码：
```
$blue : #1875e7;　
div {
　color : $blue;
}
```
生成的css 代码：
```
div {
　color : #1875e7;
}
```
如果变量需要镶嵌在字符串之中，就必须需要写在#{}之中。
```
$side : left;
　　.rounded {
　　　　border-#{$side}-radius: 5px;
　　}
```
#2. 嵌套
```
sass可以进行选择器的嵌套，表示层级关系，看起来很优雅整齐。
```
sass代码：
```
nav {
  ul {
    margin: 0;
  }

  li { display: inline-block; }

  a {
    display: block;
  }
}
```
生成的css代码：
```
nav ul {
  margin: 0;
}

nav li {
  display: inline-block;
}

nav a {
  display: block;
}
```
属性也可以嵌套，比如border-color属性，可以写成：
```
p {
　　　border: {
　　　　　color: red;
　　　}
　}
```
注意，border后面必须加上冒号。 在嵌套的代码块内，可以使用&引用父元素。比如a:hover伪类，可以写成：
```
a {
　　　&:hover { color: #ffb3ff; }
　}
```
#3. 导入
```
sass中如导入其他sass文件，最后编译为一个css文件，优于纯css的@import。其中注意的是如果sass文件的名字以“_”开头，则不会被编译成css文件
```
_reset.scss文件：
```
html,
body,
ul,
ol {
   margin: 0;
  padding: 0;
}
```
base.scss文件：
```
@import 'reset';

body {
  font-size: 100% Helvetica, sans-serif;
  background-color: #efefef;
}
```
最终生成的css:
```
html, body, ul, ol {
  margin: 0;
  padding: 0;
}

body {
  background-color: #efefef;
  font-size: 100% Helvetica, sans-serif;
}
```
#4. mixin（可以重用的代码块）
```
@mixin left {
　　　　float: left;
　　　　margin-left: 10px;
　　}
```
使用@include命令，调用这个mixin。
```
div {
　　　　@include left;
　　}
```
mixin的强大之处，在于可以指定参数和缺省值。
```
@mixin left($value: 10px) {
　　　float: left;
　　　margin-right: $value;
　}
```
#5. 扩展/继承
sass可通过@extend来实现代码组合声明，使代码更加优越简洁。<br/>
sass:
```
.message {
  border: 1px solid #ccc;
  padding: 10px;
  color: #333;
}

.success {
  @extend .message;
  border-color: green;
}

.error {
  @extend .message;
  border-color: red;
}

.warning {
  @extend .message;
  border-color: yellow;
}
```
生成的css:
```
.message, .success, .error, .warning {
  border: 1px solid #cccccc;
  padding: 10px;
  color: #333;
}

.success {
  border-color: green;
}

.error {
  border-color: red;
}

.warning {
  border-color: yellow;
}
```
#6. 运算
sass可进行简单的加减乘除运算等<br/>
sass:
```
$var:100px;
div {
　　　　margin: (14px/2);
　　　　top: 50px + 100px;
　　　　right: $var * 0.5;
　　}
```
生成的css:
```
div {
　　　　margin: 7px;
　　　　top: 150px;
　　　　right: 50px;
　　}
```
#7. 颜色
sass中集成了大量的颜色函数，让变换颜色更加简单。<br/>
如下几个颜色函数：
```
lighten(#cc3, 10%) // #d6d65c
darken(#cc3, 10%) // #a3a329
grayscale(#cc3) // #808080
complement(#cc3) // #33c
```
例子：<br/>
sass:
```
$linkColor: #08c;
a {
    text-decoration:none;
    color:$linkColor;
    &:hover{
      color:darken($linkColor,10%);
    }
}
```
生成的css:
```
a {
  text-decoration: none;
  color: #0088cc;
}
a:hover {
  color: #006699;
}
```
#8. 自定义函数
SASS允许用户编写自己的函数。
```
　@function double($n) {
　　　　@return $n * 2;
　　}
　　#sidebar {
　　　　width: double(5px);
　　}
```
生成的css:
```
#sidebar {
　　　　width: 10px;
　　}
```
如果要返回字符串，可以这样写
```
@function myurl($url){
    @return "../#{$url}";   //返回一个拼接的新地址
}
body{
    background-image: url(myurl(images/bg.jpg)); 
}
```
生成的css:
```
body {
  background-image: url("../images/bg.jpg"); }
```
#9. 条件用法
@if可以用来判断：
```
p {
　　　@if 1 + 1 == 2 { border: 1px solid; }
　　　@if 5 < 3 { border: 2px dotted; }
　}
```
配套的还有@else命令：
```
@if lightness($color) > 30% {
　　　background-color: #000;
　} @else {
　　　background-color: #fff;
　}
```
#10. 循环语句
for循环
```
@for $i from 1 to 10 {
　　　　.border-#{$i} {
　　　　　　border: #{$i}px solid blue;
　　　　}
　　}
```
while循环
```
$i: 6;
　　@while $i > 0 {
　　　　.item-#{$i} { width: 2em * $i; }
　　　　$i: $i - 2;
　　}
```
each循环
```
@each $member in a, b, c, d {
　　　　.#{$member} {
　　　　　　background-image: url("/image/#{$member}.jpg");
　　　　}
　　}
```




