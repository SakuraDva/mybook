#input-extend扩展表单功能


#搜索框
    search   搜索框       主要增加了一个快速清除内容的功能
             兼容性：IE10+以上支持

```
<h2>搜索框</h2>
<input type="search" />
```

#电话输入框
|属性|值|描述|
|:- |:-|:-|
|tel|number|主要通过搭配pattern属性来检查正确的电话号码|
|pattern|number|检验规则，通常用正则表达式来表示   []表示范围     {}表示出现的次数|
    上面两个都是必填的
     兼容性：IE10+以上浏览器支持
```
<h2>电话输入框</h2>
<input type="tel" pattern="1[0-9]{10}">
```


#颜色色板

|属性|值|描述|
|:- |:-|:-|
|name|name|定义颜色版的名称|
          兼容性：IE和Safari不支持
```
<h2>颜色色板</h2>
<input type="color" name="color"/>
```

#日期
|属性|值|描述|
|:- |:-|:-|
|datetime-local|datetime-local|可以选择年月日时间|
|date|date|可以选择年月日|
|month|month|可以选择年月|
|week|week|可以选择年月日和周几（移动端几乎不兼容）|
|time|time|可以选择时分|
       兼容性：PC端除了IE和Safari（pc）不支持
       移动端安卓和IOS全支持（除了week）

```
<h2>日期</h2>
<input type="datetime-local" name="datetiem-local" /><br />
<input type="date" name="date" /><br />
<input type="month" name="month" /><br />
<input type="week" name="week" /><br />
<input type="time" name="time" /><br />
```

#数字范围选择器
|属性|值|描述|
|:- |:-|:-|
|range|range|数字范围选择器|
|min|number|最小值|
|max|number|最大值|
|step|number|每次改动的步伐大小|
|value|value|当前默认值|
```
<h2>数字范围选择器</h2>
<input type="range" min="0" max="100" step="1" value="0"/>
```

#例子
<h2>搜索框</h2>
<input type="search" />

<h2>电话输入框</h2>
<input type="tel" pattern="1[0-9]{10}">

<h2>颜色色板</h2>
<input type="color" name="color"/>


<h2>日期</h2>
<input type="datetime-local" name="datetiem-local" /><br />
<input type="date" name="date" /><br />
<input type="month" name="month" /><br />
<input type="week" name="week" /><br />
<input type="time" name="time" /><br />



<h2>数字范围选择器</h2>
<input type="range" min="0" max="100" step="1" value="0"/>