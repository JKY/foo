# 如何使用

1. 在页面中加入 mkit.js 到 header 中;

		<script src='http://m.postio.me/mkit.js'></script>
		
2. 在 libaray 初始化完毕后掉用存储函数
		
		/* 配置成功后掉用 mkit 的功能接口 */
		var onApiReady = function(api){
			/* 数据保存接口, 替换 DATA 为自己的 JSON 对象*/
			api.store({a:1,b:2}).then(function(r) {
                console.log(r);
            });
		};
		
		/* 初始化 mkit lib */
		mkit.ready('APPID', onApiReady);
	
	## 说明
	#### 接口名称
		
		store(DATA)
		
	#### 参数
	- DATA: 需要保存的数据, JSON 对象
	#### 返回值
	- Promise
	

3. 当接口调用成功后您可以登录后台查看接收到的数据并导出;
