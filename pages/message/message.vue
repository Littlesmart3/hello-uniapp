<template>
	<view>
		<button type="primary" @click="chooseImg">上传图片</button>
		<image v-for='item in imgArr' :src="item" @click="previewImg(item)"></image>
		<!-- #ifdef  H5 -->
		<view>我希望在H5中打印</view>
		<!-- #endif -->
		<!-- #ifdef MP-WEIXIN -->
		<view>我希望在微信小程序中使用</view>
		<!-- #endif -->
	</view>
</template>

<script>
	export default {
		data() {
			return {
				imgArr: []
			}
		},
		methods: {
			chooseImg() {
				uni.chooseImage({
					count: 5,
					success: res => {
						this.imgArr = res.tempFilePaths
					}
				})
			},
			previewImg(current) {
				uni.previewImage({
					current,
					urls: this.imgArr,
					loop: true,
					indicator: 'number'
				})
			},
			onLoad() {
				// #ifdef H5
				console.log('我希望在H5中打印')
				// #endif
				// #ifdef MP-WEIXIN
				console.log('我希望在微信小程序中使用')
				// #endif
			}
		}
	}
</script>

<style>
	/* #ifdef H5 */
	view{
		color: hotpink;
	}
	/* #endif */
	/* #ifdef MP-WEIXIN */
	view{
		color: hotpink;
	}
	/* #endif */
</style>
