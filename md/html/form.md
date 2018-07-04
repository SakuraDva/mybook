#Form表单标签


|属性|值|描述|
|:-  |:-|:- |
|action|url|规定当提交表单时向何处发送表单数据。|
|name|form_name|规定表单的名称。|
|method|get,post|规定用于发送 form-data 的 HTTP 方法。|
|target|_blank,_self,_top,_parent|规定在浏览器何处打开 action URL(地址)。|
|enctype|application/x-www-form-urlencoded,multipart/form-data,text/plain|规定在发送到服务器之前应该如何对表单数据进行编码。|
|novalidate|novalidate|如果使用该属性，则提交表单时不进行验证。|
|autocomplete|on,off|规定是否启用表单的自动完成功能。|
|accept-charset|charset-list|规定服务器可处理的表单数据字符集。|


#定义和用法
    1.<form> 标签用于为用户输入创建 HTML 表单。
    2.表单能够包含 input 元素，比如文本字段、复选框、单选框、提交按钮等等。
    3.表单还可以包含 menus、textarea、fieldset、legend 和 label 元素。
    4.表单用于向服务器传输数据。



#注意
    1.get   轻量的请求方式，信息量比较小，安全要求不高(浏览产品页面，文章页面，访问一些咨询页面) 轻快低。
    2. get(信息是存放在url地址栏后面，例如以login.php?username=123&pw=123这样的形式来传输信息)。
    3.post  较重的请求方式，信息量比较大，安全要求相对要高（上传文件，上传文章，网站登录，验证等）高大尚。
    4.post(信息是存放在表单数据里面)。
    5action 接收地址，通常应该是一个后台的程序处理地址，(php,jsp,.net,nodejs)后台程序 ,如果不填则默认提交本页面。
    6.target  表单提交的页面打开方式，常用的值（_self,_blank或者是具体的窗体名字例如（iframe的名字））。
    7.name   表单的名字，主要用来区分多个表单
    8.注释：form 元素是块级元素，其前后会产生折行。

```
<form action="login.php" name="login" method="post">
	用户名： <input type="text" name="username" /><br />
	密码:   <input type="password" name="pw" /><br />
	<input type="submit" />
</form>
```

#例子
<form action="login.php" name="login" method="post">
	用户名： <input type="text" name="username" /><br />
	密码:   <input type="password" name="pw" /><br />
	<input type="submit" />
</form>