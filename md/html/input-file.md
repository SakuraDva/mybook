#input-file文件上传标签


|属性|值|描述|
|:- |:-|:-|
|capture|camera,camcirder,microphone| 可以设置打开的程序（针对移动端）|
|accept|image/*,video/*,audio/*|限制上传的文件类型(多种类型可以用逗号隔开)。|
|multiple|multiple|可以多选文件，进行上传|

#注意：
     1.如果涉及到文件上传，需要用post方式，并且form的enctype属性，要设置为multipart/form-data
    
```
头像: <input type="file" name="headerurl[]" multiple />
	 <input type="submit" /><br />
```

#例子
头像: <input type="file" name="headerurl[]" multiple />
	 <input type="submit" /><br />