<template>
	<view class="container">
		<uni-nav-bar leftIcon="search"  height="80px" :border="false"></uni-nav-bar>
		<Tabs v-model="activeTab" :scroll="false" :tabs="tabs"></Tabs>
		<uni-swiper-dot :info="swiperList" :current="activeTab">
			<swiper class="swiper-box"  @change="changeSwiper">
				<swiper-item v-for="(item ,index) in swiperList" :key="index">
					<view class="swiper-item">
						<image class="swiper-img" :src="item.img" mode="aspectFill"></image> 
					</view>
				</swiper-item>
			</swiper>
		</uni-swiper-dot>
		<view class="title-tips">快速入口</view>
		<view class="fast">
			<view v-for="(item, index) in fastList" :key="index">
				<view class="item">
					<image class="img" :src="item.img" mode="aspectFit"></image>
					<view class="text">{{item.text}}</view>
				</view>
			</view>

			
		</view>
	</view>
</template>

<script>
	import Tabs from "../../components/Tabs/Tabs.vue"
	export default {
		data() {
			return {
				activeTab: 0,
				tabs: ['关注', '推荐', '最新', '发现'],
				swiperList: [{
					img: 'https://oss.smartfish.com.cn/banner/202203011414.jpg'
				}, {
					img: 'https://oss.smartfish.com.cn/banner/202203011433.png'
				}],
				fastList: [{
					img: 'https://oss.smartfish.com.cn/other/fish-houser.png',
					text: '预约渔墅'
				},{
					img: 'https://oss.smartfish.com.cn/other/vegetable.png',
					text: '认租田地'
				},{
					img: 'https://oss.smartfish.com.cn/other/sedan.png',
					text: '预约房车'
				}]
				
			}
		},
		onLoad() {

		},
		watch: {

		},
		methods: {
			changeSwiper(e) {
				this.activeTab = e.detail.current
			},
		}
	}
</script>

<style lang="scss">
.container {
	// padding: 0 24rpx;
	.swiper-box {
		width: 100%;
		height: 320rpx;
		margin-top: 30rpx;
		padding: 0 24rpx;
		display: flex;
		justify-content: center;
		.swiper-img {
			width: 702rpx;
			height: 320rpx;
			border-radius: 20rpx;
		}
	}
	.title-tips {
		margin: 50rpx 24rpx 20rpx;
		font-size: 30rpx;
		font-weight: 700;
		color: #333333;
	}
	.fast {
		padding: 0 24rpx;
		display: grid;
		grid-row-gap: 32rpx;
		grid-column-gap: 24rpx;
		grid-template-columns: 1fr 1fr 1fr;
		.item {
			width: 218rpx;
			height: 210rpx;
			background: #ffffff;
			border-radius: 20rpx;
			box-shadow: 0rpx 2rpx 16rpx 0rpx rgba(0,0,0,0.09); 
			display: flex;
			flex-direction: column;
			align-items: center;
			justify-content: center;
			.img {
				width: 124rpx;
				height: 86rpx;
			}
			.text {
				margin-top: 24rpx;
				font-size: 28rpx;
				font-weight: 400;
				color: #333333;
			}
		}
	}
}
</style>