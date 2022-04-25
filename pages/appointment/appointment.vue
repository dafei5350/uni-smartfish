<template>
	<view class="container">
		<hx-navbar ref="hxnb" :config="navConfig" />
		<view class="header">
			<image class="img-show" src="https://oss.smartfish.com.cn/banner/order.png" mode="aspectFit"></image>	
		</view>
		<view class="body">
			<Search></Search>
			<view class="list" v-for="(item,index) in 10" :key="index">
	
					<view class="item">
						<view class="image">
							<image class="img-case" src="https://app.smartfish.com.cn/Files/project/hy_xc_ys_1_1.png" mode="aspectFill"></image>
						</view>
						<view class="title">
							<view class="text">尹家湾渔墅</view>
							<view class="avatar"></view>
						</view>
						<view class="address">
							<uni-icons type="location" size="15"></uni-icons>
							<text class="ad-text">深圳市宝安区改成二路黄田公园</text>
						</view>
						<view class="action">
							<view class="like">
								<uni-icons type="hand-up" color="#a3a3a3" size="30"></uni-icons>
								<text>99</text>
							</view>
							<view class="see">
								<uni-icons type="eye" color="#a3a3a3" size="30"></uni-icons>
								<text>99</text>
							</view>
							<view class="comment">
								<uni-icons type="chatboxes" color="#a3a3a3" size="30"></uni-icons>
								<text>99</text>
							</view>
							
						</view>
					</view>
				
			</view>
		</view>
	</view>
</template>

<script>
	import Search from "../../components/Search/Search.vue"
	export default {
		data() {
			return {
				navConfig: {
					back: false,
					title: '预约',
					
				}
			};
		}
	}
</script>

<style lang="scss">
	page {
		// background-color: #f5f5f5;
	}
	.container {
		width: 100%;
		
		display: flex;
		flex-direction: column;
		align-items: center;

		.header {
			width: 100%;
			display: flex;
			flex-direction: column;
			align-items: center;
			background-color: white;
			// padding-bottom: 30rpx;
			
			.img-show {
				width: 702rpx;
				height: 264rpx;
				border-radius: 20rpx;
			}
		}
		
		.body {
			width: 100%;
			display: flex;
			flex-direction: column;
			align-items: center;
			padding: 0 24rpx;
			margin: 30rpx 0 100rpx 0;
			
			.list {
				width: 100%;
				margin-top: 30rpx;
				display: flex;
				justify-content: center;
				.item {
					width: 702rpx;
					height: auto;
					margin-top: 10rpx;
					border-radius: 20rpx;
					box-shadow: rgba(99, 99, 99, 0.2) 0px 2px 8px 0px;
					touch-action: pan-y; 
					
					.image {
						.img-case {
							width: 702rpx;
							height: 358rpx;
							border-top-left-radius: 20rpx;
							border-top-right-radius: 20rpx;
						}
					}
					
					.title {
						margin-top: 24rpx;
						padding: 0 24rpx;
						display: flex;
						justify-content: space-between;
						
						.text {
							font-size: 36rpx;
							font-weight: 700;
							color: #333333;
						}
						.avatar {
							width: 272rpx;
							height: 52rpx;
							background: #f5f5f5;
							border-radius: 26rpx;
						}
					}
					.address {
						margin-top: 10rpx;
						padding: 0 24rpx;
						font-size: 24rpx;
						font-weight: 400;
						color: #999999;
					}
					.action {
						padding: 30rpx 24rpx;
						display: flex;
						justify-content: space-around;
						
						view {
							display: flex;
							align-items: center;
							
							text {
								font-size: 20rpx;
								font-weight: 400;
								color: #999999;
								margin-left: 10rpx;
							}
						}
					}
				}
			}
		}
	}
</style>
