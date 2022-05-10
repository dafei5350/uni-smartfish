<template>
	<view class="container">
		<view class="main">
			<view class="header">
				<view class="action">
					<image class="avatar" src="@/static/tabbar/my1.png" mode="aspectFit"></image>
					<view class="userinfo">
						<view class="name">怪狗</view>
						<view class="time">2022年5月5日</view>
					</view>
				</view>
				<view class="action" @click="onMore">
					<uni-icons type="more-filled" size="20"></uni-icons>
				</view>
			</view>
			<view class="body">
				<view class="content">
					你的气质里藏着你走过的路、读过的书以及你爱过的人。 
				</view>
				<view class="img-grup">
					<template v-for="(item, index) in 5">
						<image class="thumb" src="https://oss.smartfish.com.cn/temp/test.jpg" mode="aspectFill"></image>
					</template>
				</view>
			</view>
			<view class="footer">
				<view class="ico-item">
					<uni-icons type="paperplane" size="25"></uni-icons>
					<view class="num">分享</view>
				</view>
				<view class="ico-item">
					<uni-icons type="chat" size="25"></uni-icons>
					<view class="num">99</view>
				</view>
				<view class="ico-item" @click="onLike">
					<uni-icons :type="isLike?'hand-up':'hand-up-filled'" :color="isLike?'':'#ff4757'" size="25"></uni-icons>
					<view class="num">99</view>
				</view>
				
			</view>
		</view>
		<view class="more" v-if="isMore">
			
		</view>
	</view>
</template>

<script>
	export default {
		name:"TellAbout",
		data() {
			return {
				isMore: false,
				isLike: false
			};
		},
		methods: {
			onLike() {
				this.isLike = !this.isLike
			},
			onMore() {
				this.isMore = true
			}
		}

	}
</script>

<style lang="scss" scoped>
.container {
	
	.main {
		border-radius: 20rpx;
		padding: 24rpx;
		margin-top: 30rpx;
		box-shadow: rgba(0, 0, 0, 0.1) 0px 1px 3px 0px, rgba(0, 0, 0, 0.06) 0px 1px 2px 0px;
		.header {
			width: 100%;
			display: flex;
			justify-content: space-between;
			.action {
				display: flex;
				align-items: center;
				.avatar {
					width: 80rpx;
					height: 80rpx;
					border-radius: 50%;
				}
				.userinfo {
					margin-left: 20rpx;
					.name {
						font-size: 26rpx;
						font-weight: 700;
						color: #333333;
					}
					.time {
						font-size: 20rpx;
						font-weight: 400;
						color: #999999;
					}
				}
			}
		}
		.body {
			
			.content {
				margin-top: 30rpx;
				font-size: 30rpx;
				font-weight: 400;
				color: #333333;
			}
			.img-grup {
				margin-top: 30rpx;
				display: grid;
				grid-row-gap: 10rpx;
				grid-column-gap: 10rpx;
				grid-template-columns: 1fr 1fr 1fr;

				.thumb {
					width: 200rpx;
					height: 200rpx;
					border-radius: 20rpx;
				}
			}
		}
		.footer {
			height: 70rpx;
			display: flex;
			align-items: flex-end;
			justify-content: flex-end;
			.ico-item {
				display: flex;
				align-items: center;
				margin-left: 50rpx;
				.num {
					margin-left: 5rpx;
				}
			}
		}
	}
}
</style>