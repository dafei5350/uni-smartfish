<template>
	<view>
		<video 
			id="myVideo" 
			class="content" 
			object-fit="fill" 
			:enable-play-gesture="false" 
			:enable-progress-gesture="false" 
			:show-loading="false" 
			:show-center-play-btn="false" 
			src="https://oss.smartfish.com.cn/temp/bg-login.mp4" 
			:autoplay="true" 
			:loop="true" 
			:controls="false">
			<cover-view class="xz-title" style="">
				让农民没有荒地
			</cover-view>
			<cover-view class="xz-button-1" @click="onLogin">
				微信一键登入
			</cover-view>
		</video>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				
			}
		},
		methods: {
			onLogin() {
				console.log("log");
			}
		}
	}
</script>

<style>
.content{
	width: 750rpx;
	height: 100%;
	/* z-index: 9; */
	position: fixed;
	top: 0;
	left: 0;
	bottom: 0;
	right: 0;
	background-color: #007AFF;
}
.xz-title{
	width: 600rpx;
	height: 90rpx;
	position: fixed;
	bottom: 400rpx;
	margin-left: 40rpx;
	border-radius: 12rpx;
	line-height: 90rpx;
	color: #FFFFFF;
	font-size: 30rpx;
	/* text-shadow: 5px 5px 5px #FF0000; */
}
.xz-button-1{
	width: 250rpx;
	height: 90rpx;
	position: fixed;
	bottom: 305rpx;
	margin-left: 40rpx;
	background-color: #FFFFFF;
	border-radius: 12rpx;
	display: flex;
	justify-content: center;
	align-items: center;
	text-align: center;
	line-height: 90rpx;
}
.xz-button-2{
	width: 250rpx;
	height: 90rpx;
	position: fixed;
	bottom: 300rpx;
	margin-left: 320rpx;
	border:4rpx solid #FFFFFF;
	border-radius: 12rpx;
	text-align: center;
	line-height: 90rpx;
	color: #FFFFFF;
}
</style>
