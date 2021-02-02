<template>
	<view class="content">
		关于
	</view>
</template>

<script>
	export default {
		data() {
			return {
				title: 'Hello'
			}
		},
		onShow() { //监听页面显示
			var url = 'http://api.com'
			// 使用 Mock
			var Mock = require('mockjs')
			var data = Mock.mock(url,{
			    // 属性 list 的值是一个数组，其中含有 1 到 10 个元素
			    'list|1-10': [{
			        // 属性 id 是一个自增数，起始值为 1，每次增 1
			        'id|+1': 1
			    }]
			})
			// 输出结果
			// console.log(JSON.stringify(data, null, 4))
			
			uni.request({
			    url: url, //仅为示例，并非真实接口地址。
				method:'post',
			    success: (res) => {
			        console.log(res);
			    }
			});
			
			uni.setStorage({ //存储数据   设置的是localStorage
			    key: 'storage_key',
			    data: 'hello',
			    success: function () {
			        console.log('设置缓存success');
			    }
			});
			uni.getStorage({ //获取数据
			    key: 'storage_key',
			    success: function (res) {
			        console.log(res.data);
			    }
			});
			uni.removeStorage({ //删除数据
			    key: 'storage_key',
			    success: function (res) {
			        console.log('删除success');
			    }
			});
			
			// uni.chooseImage({
			//     count: 6, //默认9
			//     success: function (res) {
			//         console.log(res.tempFilePaths);
			//     }
			// });
		},
		
		methods: {
			
		},
		mounted() {
			
		}
	}
</script>

<style lang="scss">

</style>
