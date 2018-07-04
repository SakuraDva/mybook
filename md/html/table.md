#table表格标签

|属性|说明|
|:-  |:-  |
|width|规定表格的宽度。(固定值和百分比)|
|heigth|规定表格的高度。(固定值和百分比)|
|border|规定表格边框的宽度。|
|align|对齐方式 left center right|
|cellspacing|单元格与单元格之间的间距(边框对边框距离)|
|cellspacing|文字与边框的距离（边框与文字之间的距离）|
|rules|规定内侧边框的哪个部分是可见的。(none,groups,rows,cols,all)|
|valign|垂直排列方式(top,middle,bottom)|

#解释
        table标签
        	tr 表示一行
        	td 表示一个单元格
        	table>tr*想要的数行>td*输入想要的列（快速建立表格）
        	table>tr*想要的数行>td{输入}*输入想要的列（快速建立表格）





#合并单元格
    合并单元格
    合并列：colspan
    合并行：rowspan
    背景色：bgcolor
    不管合并与否，一定要保证每一行的td数量必须一致
    列的合并口诀：1.先找到要合并的最左边的单元格
               2.加colspan属性，值是被合并的单元格的个数
               3.把被合并的单元格删除或注销
    行的合并口诀：1.先找到要合并的最左边的单元格
               2.加rowspan属性，值是被合并的单元格的个数
               3.把被合并的单元格删除或注销


```
<table width="90%"  height="800" border="1" align="center" cellspacing="0" cellpadding="10px">
	<tr>
		<td>单元格1</td>
		<td>单元格2</td>
		<td>单元格3</td>
	</tr>
	<tr>
		<td>单元格1</td>
		<td>单元格2</td>
		<td>单元格3</td>
	</tr>
	<tr>
		<td>单元格1</td>
		<td>单元格2</td>
		<td>单元格3</td>
	</tr>
	<tr>
		<td>单元格1</td>
		<td>单元格2</td>
		<td>单元格3</td>
	</tr>
</table>
```
#例子(普通表格)
<table width="90%"  height="800" border="1" align="center" cellspacing="0" cellpadding="10px">
	<tr>
		<td>单元格1</td>
		<td>单元格2</td>
		<td>单元格3</td>
	</tr>
	<tr>
		<td>单元格1</td>
		<td>单元格2</td>
		<td>单元格3</td>
	</tr>
	<tr>
		<td>单元格1</td>
		<td>单元格2</td>
		<td>单元格3</td>
	</tr>
	<tr>
		<td>单元格1</td>
		<td>单元格2</td>
		<td>单元格3</td>
	</tr>
</table>
#例子(合并单元格)
<table border="1" align="center">
	<tr>
		<td align="center" colspan="2">单元格1</td>
		<!--<td align="center">单元格2</td>
		<td align="center">单元格3</td>-->
	</tr>
	<tr>
		<td align="center" rowspan="2">单元格1</td>
		<td align="center">单元格2</td>
		<td align="center">单元格3</td>
	</tr>
	<tr>
		<!--<td align="center">单元格1</td>
		<td align="center">单元格2</td>-->
		<td align="center">单元格3</td>
	</tr>
</table>
#心得
1.它是用来表示制作表格的，tr是行，td是单元格
2.因为有些数据是要用到表格来进行存放的
3.用来制作表格数据时使用