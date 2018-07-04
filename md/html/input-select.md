#input-select下拉框标签

|属性|值|描述|
|:- |:-|:-|
|multiple|multiple|加上该属性，则变为多选模式|
|name|name|规定一个select的名称|
|optgroup|label|向里面定义一个值，这个值在下拉列表中不能选定|

#注意：
    1.select和option是固定的组合，缺一不可

```
<select name="city" id="" multiple>
				<optgroup label="广东省">
						<option value="1">广州</option>
						<option value="2">深圳</option>
						<option value="3">清远</option>
						<option value="4">茂名</option>
						<option value="5">汕头</option>
						<option value="6">汕尾</option>
						<option value="7">揭阳</option>
				</optgroup>
				<optgroup label="其它省">
					    <option value="8">北京</option>
					    <option value="9">杭州</option>
					    <option value="10">上海</option>
				</optgroup>
</select><br />
```

#例子
所在城市:
<select name="city" id="" multiple>
			<optgroup label="广东省">
					<option value="1">广州</option>
					<option value="2">深圳</option>
					<option value="3">清远</option>
					<option value="4">茂名</option>
					<option value="5">汕头</option>
					<option value="6">汕尾</option>
					<option value="7">揭阳</option>
			</optgroup>
			<optgroup label="其它省">
				    <option value="8">北京</option>
				    <option value="9">杭州</option>
				    <option value="10">上海</option>
			</optgroup>
		</select><br />
