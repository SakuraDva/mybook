#input-radio单选框

|属性|值|描述|
|:- |:-|:-|
|checked|checked|表示选中的状态（单选框只允许设置其中一个为checked）|
|name|name|需要保证多个单选选项的名字都是一样的|
|value|value|该数据所对应的值|
|lable|for|关联属性(填写被关联的标签的id)|



```
性别: <label for="man">男</label><input  id="man" type="radio" name="sex"  value="1"  checked/> / <label for="lady">女</label><input id="lady" type="radio" name="sex" value="2"  /><br />
```
#例子
性别: <label for="man">男</label><input  id="man" type="radio" name="sex"  value="1"  checked/> / <label for="lady">女</label><input id="lady" type="radio" name="sex" value="2"  /><br />