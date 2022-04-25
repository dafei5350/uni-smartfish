<template>
	<view class="search" style="background-color: white;">
		<view class="main" style="background-color: #f5f5f5;">
			<uni-icons type="search" color="#9f9f9f" size="30"></uni-icons>
			<input type="text" :value="searchKey" :placeholder="tips" class="search" placeholder-class="search-tips">
		</view>

	</view>
</template>

<script>
	export default {
		name:"search",
		data() {
			return {
				searchKey: '',
				tips: '搜索资源（水库/渔墅/田地/山林名称等）'
			};
		}
	}
</script>

<style lang="scss">
.search {
	width: 100%;
	height: 120rpx;
	display: flex;
	align-items: center;
	justify-content: center;

	.main {
		width: 100%;
		height: 88rpx;
		background: #f5f5f5;
		border-radius: 44rpx;
		padding: 0 30rpx;
		margin: 0 24rpx;
		display: flex;
		align-items: center;
		.search {
			margin-right: 15rpx;
		}
		.search-tips {
			font-size: 28rpx;
			font-weight: 400;
			color: #999999;
		}
	}
}

</style>