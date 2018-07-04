#DIV块级元素

|属性|说明|
|:-  |:-  |
|align|规定 div 元素中的内容的对齐方式。(left,right,center)|

#解释：
       特点：无色无味，透明的一个容器
       块级元素特点：自己占一行
    p h div 这类型的标签都具备相同特点，就是自己占一行，我们称之为块级元素。
        注释：<div> 是一个块级元素，也就是说，浏览器通常会在 div 元素前后放置一个换行符。
#用法：
    <div> 是一个块级元素。这意味着它的内容自动地开始一个新行。实际上，换行是 <div> 固有的唯一格式表现。可以通过 <div> 的 class 或 id 应用额外的样式。
      可以对同一个 <div> 元素应用 class 或 id 属性，但是更常见的情况是只应用其中一种。这两者的主要差异是，class 用于元素组（类似的元素，或者可以理解为某一类元素），而 id 用于标识单独的唯一的元素。
```
<div style="color:#00FF00">
  <h3>This is a header</h3>
  <p>This is a paragraph.</p>
</div>
```

#例子
<div style="color:#00FF00">
  <h3>This is a header</h3>
  <p>This is a paragraph.</p>
</div>
#心得
1.它是一个无色无味的一个容器
2.因为它里面可以放很多的内容，也可以应用多个class属性
3.套用css属性时