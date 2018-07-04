#Input多功能标签


|属性|值|描述|
|:- |:-|:-|
|accept|mime_type|规定通过文件上传来提交的文件的类型。|
|type|button,checkbox,text,submit,hidden等|规定 input 元素的类型属性，决定了这个input的功能，如果没有设置或设置不合法的值，则全部默认认为text（单行输入框）|
|name|field_name|定义 input 元素的名称。(该数据所对应的名字，主要是给后台获取数据时使用。)|
|value|value|规定 input 元素的值。(该数据所对应的值,如果不填则默认为空)|
|size|number_of_char|定义输入字段的宽度。(控制输入框的显示长度)|
|disabled|disabled|当 input 元素加载时禁用此元素。(表示禁用该输入框，连数据传输也停止。(禁止输入和禁止提交该数据))|
|readonly|readonly|	规定输入字段为只读。(只读，禁止输入，但允许提交)|
|maxlength|number|规定输入字段中的字符的最大长度。(该数据的值所允许的最大字符长度)|
|placeholder|text|规定帮助用户填写输入字段的提示。(提示语属性)|
|required|required|	指示输入字段的值是必需的。|
|sec|URL|定义以提交按钮形式显示的图像的 URL。|
|step|number|规定输入字的的合法数字间隔。|
|pattern|regexp_pattern|规定输入字段的值的模式或格式。(例如 pattern="[0-9]" 表示输入值必须是 0 与 9 之间的数字。)|
|alt|text|定义图像输入的替代文本。|
|autofocus|autofocus|规定输入字段在页面加载时是否获得焦点。（不适用于 type="hidden"）|
|checked|checked|规定此 input 元素首次加载时应当被选中。|
|autocomplete|on,off|规定是否使用输入字段的自动完成功能。|
|form|formname|规定输入字段所属的一个或多个表单。|
|formaction|URL|覆盖表单的 action 属性。（适用于 type="submit" 和 type="image"）|
|formenctype|formenctypename|覆盖表单的 enctype 属性。（适用于 type="submit" 和 type="image"）|
|formmethod|get,post|覆盖表单的 method 属性。（适用于 type="submit" 和 type="image"）|
|height|pixels,%|定义 input 字段的高度。（适用于 type="image"）|
|list|datalist-id|引用包含输入字段的预定义选项的 datalist 。|
|max|number,date|规定输入字段的最小值。(请与 "max" 属性配合使用，来创建合法值的范围。)|
|width|pixels,%|定义 input 字段的宽度。（适用于 type="image"）|

#input type属性
button,checkbox,text,submit,hidden,reset,radio,password,file,image
```
用户名： <input type="text" maxlength="5" placeholder="请输入用户名"/><br />
密码:  <input type="password" name="pw" placeholder="请输入密码"/><br />
```

#例子
用户名： <input type="text" maxlength="5" placeholder="请输入用户名"/><br />
密码:  <input type="password" name="pw" placeholder="请输入密码"/><br />


#链接
input更对属性http://www.w3school.com.cn/tags/tag_input.asp;
