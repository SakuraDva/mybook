#Sass的玩法

#命令行玩起
##1. 最基础用法
把scss文件转换为css文件。<br/>
使用方法：scss 目标scss文件 生成的css文件
```
scss common.scss common.css
```
##2. 实时监测修改
实时监控某个文件夹内的scss文件，并实时转换为css文件<br/>
使用方法：scss --watch 监测目录:生成目录
```
scss --watch source:css
 注意：监测的目录不宜过深，最好可以用相对路径作为监测目录路径，有效的加快监测效率。
```
##3. 选择生成的风格
```
　　* nested：嵌套缩进的css代码，它是默认值。
　　* expanded：没有缩进的、扩展的css代码。
　　* compact：简洁格式的css代码。
　　* compressed：压缩后的css代码。
```
例如：scss文件转换为压缩后的css文件：
```
scss common.scss common.css  --style compressed
```
例如：实时监测并转换为压缩后的css文件：
```
scss --watch source:css --style compressed
```
#常用的一些技巧
1. 动态计算百分比
```
$dw:750;            //设计图的宽度
@function percent($px){
 @return $px/$dw*100%;
}
.logo {
 width: percent(100);  //动态计算百分比宽
}
```
2. 设计图尺寸除2，求出移动端的尺寸 
```
@function d($px){
 @return $px/2;
}
.logo {
 width: d(100px);  //动态计算宽
}
```
3. 动态计算rem
```
$font-size : 20px;  //页面的根字体大小
@function r($px){
 @return $px/$font-size*1rem;
}
```




