#magin相邻的奇异现象


##触发现象和解决办法
触发margin父子相邻的怪异现象条件<br/>
 1. 儿子必须是块级元素<br/>
 2. 该儿子直接与父亲相邻
	
解决办法：<br/>
1. 改变儿子的display<br/>
2. 用父亲的padding-top来代替儿子margin-top

###案例
	<head>
		<meta charset="UTF-8">
		<title></title>
	</head>
	<body>
		<style>
			/**
			 * 触发margin父子相邻的怪异现象条件
			 * 1. 儿子必须是块级元素
			 * 2. 该儿子直接与父亲相邻
			 * 
			 * 解决办法：
			 * 1. 改变儿子的display
			 * 2. 用父亲的padding-top来代替儿子margin-top
			 */
			.baba{
				height: 500px;
				background: lightyellow;
			}
			.son{
				display: inline-block;
				height: 100px;
				width: 100px;
				background: skyblue;
				margin-top: 100px;
			}
		</style>
		<div class="baba">
			<div class="son">
				
			</div>
		</div>
		
		
	</body>