<template>
	<view class="container">
		<hx-navbar ref="hxnb" :config="config" />
		1
	</view>
</template>

<script>
	export default {
		data() {
			return {
				config:{
									back: false,
									color: '#ffffff',
									title: '预约'
							},
			};
		}
	}
</script>

<style lang="scss">

</style>
