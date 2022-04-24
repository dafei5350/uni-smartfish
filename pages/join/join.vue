<template>
	<view class="container">
		<uni-swiper-dot :info="swiperList" :current="swiperCur">
			<swiper class="swiper-box"  @change="changeSwiper">
				<swiper-item v-for="(item ,index) in swiperList" :key="index">
					<view class="swiper-item">
						<image class="swiper-img" :src="item.img" mode="aspectFill"></image> 
						<view class="swiper-title">
							{{item.title}}
						</view>
					</view>
				</swiper-item>
			</swiper>
		</uni-swiper-dot>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				swiperCur: 0,
				swiperList: [{
					img: 'https://oss.smartfish.com.cn/swiper/swiper-item01.png',
					title: '参与田地成为农场主',
					url: ''
				},{
					img: 'https://oss.smartfish.com.cn/swiper/swiper-item03.jpg',
					title: '参与智能渔墅项目',
					url: ''
				}]
			};
		},
		methods: {
			changeSwiper(e) {
				this.swiperCur = e.detail.current
			},
		}
	}
</script>

<style lang="scss">
	page {
		width: 100%;
		height: 100%;
	}
.container {
	width: 100%;
	height: 100%;
	.swiper-box {
		width: 100%;
		height: 100vh;		
		position: relative;
		.swiper-item {
				width: 100%;
				height: 95%;		

			.swiper-img {
				width: 100%;
				height: 100%;		
			}
			.swiper-title {
				width: 602rpx;
				height: 88rpx;
				border: 2rpx solid #ffffff;
				border-radius: 46rpx;
				position: absolute;
				left: 75rpx;
				bottom: 150rpx;
				font-size: 36rpx;
				font-weight: 700;
				color: #ffffff;
				display: flex;
				align-items: center;
				justify-content: center;
			}
		}
	}
	
}
</style>
