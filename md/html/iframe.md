#iframe内嵌框架标签

|属性|值|描述|
|:-  |:-|:-  |
|align|left,right,top,middle,bottom|规定如何根据周围的元素来对齐此框架。|
|height|px,%|规定 iframe 的高度。|
|longdesc|url|规定一个页面，该页面包含了有关 iframe 的较长描述。|
|marginheigt|px|定义 iframe 的顶部和底部的边距。|
|marginwidth|px|定义 iframe 的左侧和右侧的边距。|
|name|frame_name|规定 iframe 的名称。|
|sandbox|"",allow-forms,allow-same-origin,allow-scripts,allow-top-navigation|启用一系列对&lt;iframe&gt;中内容的额外限制。|
|scrolling|yes(一直显示滚动条),no(禁止滚动),auto(自动)|规定是否在 iframe 中显示滚动条。|
|seamless|seamless|规定 &lt;iframe&gt;看上去像是包含文档的一部分。|
|src|url|规定在 iframe 中显示的文档的 URL。|
|srcdoc|HTML_code|规定在 &lt;iframe&gt; 中显示的页面的 HTML 内容。|
|width|px,%|定义 iframe 的宽度。|


#注意
    用“//”开头的资源链接，表示，自动选择请求协议，http,https


```
<iframe 
	src="http://www.baidu.com" 
	frameborder="0"
	style="width: 100%; height: 100%;"
	scrolling="no"
></iframe>
```

#例子
<iframe 
	src="http://www.baidu.com" 
	frameborder="0"
	style="width: 100%; height: 100%;"
	scrolling="no"
></iframe>