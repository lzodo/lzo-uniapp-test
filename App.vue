<script>
	export default {
		//应用的生命周期
		onLaunch: function() { //uniapp初始化完成触发(全程只触发一次)
			console.log('App Launch')
		},
		onShow: function() { //uniapp启动,或从后台到前台触发
			console.log('App Show')
		},
		onHide: function() { //uniapp从前台到后台触发
			console.log('App Hide')
		},
		onError: function() { //uniapp 报错触发
			console.log('App Error')
		}
	}
</script>

<style>
	/*每个页面公共css */
</style>
