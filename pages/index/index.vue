<template>
	<view class="content">
		<image class="logo" src="/static/logo.png"></image>
		<view class="text-area">
			<text class="title">{{title}}</text>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				title: 'Hello'
			}
		},
		onLoad(option) {
			//监听页面加载 ，并拿到上级页面传递的参数
			//只会触发一次页面切换时不会触发
			console.log("页面加载了"+ option)
		},
		onShow() { //监听页面显示
			console.log("页面出现在屏幕上了")
		},
		onReady() { //监听页面初次渲染完成 
			console.log("监听页面初次渲染完成 ")
		},
		onHide() { //监听页面隐藏
			console.log("页面隐藏")
		},
		onUnload() { //讲台页面卸载
			console.log("页面卸载")
		},
		onPullDownRefresh(){
			console.log("用户下拉页面了")
			uni.stopPullDownRefresh()
		},
		onReachBottom(){ //触底时触发
			console.log("用户上拉")
		},
		methods: {

		}
	}
</script>

<style>
	.content {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
	}

	.logo {
		height: 200rpx;
		width: 200rpx;
		margin-top: 200rpx;
		margin-left: auto;
		margin-right: auto;
		margin-bottom: 50rpx;
	}

	.text-area {
		display: flex;
		justify-content: center;
	}

	.title {
		font-size: 36rpx;
		color: #8f8f94;
	}
</style>
