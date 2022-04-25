<template>
	<view class="container">
		<view class="header">
			<image class="bg" src="https://oss.smartfish.com.cn/other/bg-my-header.png" mode="aspectFill"></image>
		</view>
		<view class="body">
			<view class="user">
				<view class="msg">
					<view class="action">
						<image class="avatar" src="../../static/logo.png" mode="aspectFit"></image>
						<view class="block">
							<view class="name">weiliang</view>
							<view class="tips">介绍自己更容易获得关注哦</view>
						</view>
					</view>
					<view class="sign-in">签到</view>
				</view>
				<view class="per-data">
					<view class="item">
						<view class="num">99</view>
						<view class="text">发布</view>
					</view>
					<view class="item">
						<view class="num">99</view>
						<view class="text">发布</view>
					</view>
					<view class="item">
						<view class="num">99</view>
						<view class="text">发布</view>
					</view>
					<view class="item">
						<view class="num">99</view>
						<view class="text">发布</view>
					</view>
				</view>
			</view>
			<view class="banner">
				<view class="equity">
					<view class="action">
						<image class="huangguan" src="https://oss.smartfish.com.cn/other/icon-crown.png" mode="aspectFit"></image>
						<view class="title">我的权益</view>
					</view>
					<view class="action">
						<view class="tips">房车体验0天/渔墅体验0天</view>
					</view>
				</view>
				<view class="order">
					<view class="item">
						<image class="img-ico" src="https://oss.smartfish.com.cn/other/my-bookings.png" mode="aspectFit"></image>
						<view class="text">我的预订</view>
					</view>
					<view class="line"></view>
					<view class="item">
						<image class="img-ico" src="https://oss.smartfish.com.cn/other/my-bookings.png" mode="aspectFit"></image>
						<view class="text">我的预订</view>
					</view>
				</view>
				<view class="serve">
					<view class="title">我的服务</view>
					<view class="options">
						<view class="items">
							<image class="img-item" src="https://oss.smartfish.com.cn/other/icon-wallet.png" mode="aspectFit"></image>
							<view class="text">我的钱包</view>
						</view>
						<view class="items">
							<image class="img-item" src="https://oss.smartfish.com.cn/other/icon-wallet.png" mode="aspectFit"></image>
							<view class="text">我的钱包</view>
						</view>
						<view class="items">
							<image class="img-item" src="https://oss.smartfish.com.cn/other/icon-wallet.png" mode="aspectFit"></image>
							<view class="text">我的钱包</view>
						</view>
						<view class="items">
							<image class="img-item" src="https://oss.smartfish.com.cn/other/icon-wallet.png" mode="aspectFit"></image>
							<view class="text">我的钱包</view>
						</view>
						<view class="items">
							<image class="img-item" src="https://oss.smartfish.com.cn/other/icon-wallet.png" mode="aspectFit"></image>
							<view class="text">我的钱包</view>
						</view>
					</view>
				</view>
				<view class="entry">
					<view class="list" v-for="(index, item) in 6" :key="index">
						
						<view class="item" >
							<view class="action">
								<uni-icons type="auth-filled" size="25"></uni-icons>
								<view class="title">实名认证</view>
							</view>
							<view class="action">
								<uni-icons type="right" size="25"></uni-icons>
							</view>
						</view>
						<view class="line"></view>
					</view>
				</view>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				
			};
		}
	}
</script>

<style lang="scss">
	page {
		background-color: #f8f9fb;
	}
.container {
	width: 100%;
	
	.header {
		width: 100%;
		height: 306rpx;
		position: relative;
		top: 0;
		
		.bg {
			width: 100%;
			height: 306rpx;
			position: absolute;
			top: 0;
		}
	}
	
	.body {
		width: 100%;
		height: 100px;
		
		position: relative;
		top: -80rpx;
		
		.user {
			width: 750rpx;
			height: 390rpx;
			background: #ffffff;
			border-radius: 40rpx 40rpx 0rpx 0rpx;
			.msg {
				display: flex;
				align-items: center;
				padding: 48rpx 24rpx 30rpx;
				justify-content: space-between;
				.action {
					display: flex;
					.avatar {
						width: 128rpx;
						height: 128rpx;
						border-radius: 50%;
					}
					.block {
						margin-left: 24rpx;
						display: flex;
						flex-direction: column;
						justify-content: center;
						.name {
							font-size: 36rpx;
							font-weight: 700;
							color: #333333;
							line-height: 32rpx;
						}
						.tips {
							margin-top: 15rpx;
							font-size: 24rpx;
							font-weight: 400;
							text-align: left;
							color: #666666;
						}
					}
				}
				.sign-in {
					width: 118rpx;
					height: 60rpx;
					background: #47bcff;
					border-radius: 30rpx;
					font-size: 30rpx;
					font-weight: 700;
					color: #ffffff;
					display: flex;
					align-items: center;
					justify-content: center;
				}

			}
			
			.per-data {
				width: 702rpx;
				height: 136rpx;
				background: #f4f8fb;
				border-radius: 20rpx;
				margin: 30rpx 24rpx 0;
				display: flex;
				align-items: center;
				justify-content: space-around;
				
				.item {
					
					.num {
						font-size: 36rpx;
						font-weight: 700;
						color: #333333;
					}
					.text {
						font-size: 24rpx;
						font-weight: 400;
						color: #333333;
					}
				}
			}
		}
		.banner {
			width: 702rpx;
			height: 116rpx;
			background: #ffffff;
			border-radius: 20rpx;
			margin: 30rpx 24rpx 0;
			position: relative;
			top: 0;
			.equity {
				
				height: 126rpx;
				background: linear-gradient(124deg,#262221 10%, #474038 85%, #484033 85%);
				border-radius: 20rpx;
				padding: 20rpx 24rpx 0;
				display: flex;
				justify-content: space-between;
				
				.action {
					
					display: flex;
					align-items: flex-start;
					.huangguan {
						width: 58rpx;
						height: 54rpx;
					}
					.title {
						font-size: 30rpx;
						font-weight: 700;
						color: #f9deaf;
						margin-left: 20rpx;
					}
					.tips {
						font-size: 28rpx;
						font-weight: 400;
						color: #f9deaf;
					}
				}
			}
			.order {
				width: 702rpx;
				height: 116rpx;
				background: #ffffff;
				border-radius: 20rpx;
				position: absolute;
				top: 90rpx;
				display: flex;
				align-items: center;
				justify-content: space-around;
				.item {
					display: flex;
					align-items: center;
					justify-content: center;
					.img-ico {
						width: 68rpx;
						height: 68rpx;
					}
					.text {
						margin-left: 30rpx;
						font-size: 30rpx;
						font-weight: 700;
						color: #333333;
					}
				}
				.line {
					width: 2rpx;
					height: 60rpx;
					background-color: #ececec;
				}
			}
		}
		.serve {
			width: 702rpx;
			height: 356rpx;
			background: #ffffff;
			border-radius: 20rpx;
			margin-top: 90rpx;
			.title {
				font-size: 30rpx;
				font-weight: 700;
				color: #333333;
				padding: 24rpx 30rpx 0;
			}
			.options {
				margin-top: 36rpx;
				display: grid;
				grid-row-gap: 32rpx;
				grid-column-gap: 40rpx;
				grid-template-columns: 1fr 1fr 1fr;
				.items {
					display: flex;
					flex-direction: column;
					align-items: center;
					justify-content: center;
					
					
					.img-item {
						width: 48rpx;
						height: 48rpx;
					}
					.text {
						font-size: 24rpx;
						font-weight: 400;
						color: #333333;
					}
				}
			}
		}
		.entry {
			width: 702rpx;
			height: auto;
			margin: 24rpx 0 30rpx;
			background: #ffffff;
			border-radius: 20rpx;
			
			.list {
				display: flex;
				flex-direction: column;
				
				.item {
					width: 100%;
					height: 110rpx;
					display: flex;
					align-items: center;
					justify-content: space-between;
					border-bottom: 1rpx solid #eeeeee;
					
					.action {
						display: flex;
						align-items: center;
						margin: 0 24rpx;
						.title {
							margin-left: 16rpx;
							font-size: 28rpx;
							font-weight: 700;
							color: #333333;
						}
					}
				}
				.line {
					
					
				}
			}
		}
	}
}
</style>
