<template>
	<view>
		<button @click="get">发送get请求</button>
		<view>这是列表页</view>
		<view class="box-item" v-for="item in list">
			{{item}}
		</view>
		<!-- <button @click="pullDown">下拉刷新</button> -->
	</view>
</template>

<script>
	export default{
		data(){
			return{
				list:['前端','JAVA','Python','javascript','大数据','前端','JAVA','Python','javascript','大数据']
			}
		},
		onPullDownRefresh(){
			console.log("触发了下拉刷新！")
			setTimeout(() => {
				this.list=['JAVA','Python','javascript','大数据','前端']
				uni.stopPullDownRefresh()
			},2000)
		},
		onReachBottom(){
			console.log("页面触底了")
			this.list=[...this.list,...['JAVA','Python','javascript','大数据','前端']]
		},
		methods:{
			pullDown() {
				uni.startPullDownRefresh()
			},
			get() {
				uni.request({
					url:"http://localhost:8082/api/getlunbo",
					success(res){
						console.log(res)
					}
				})
			}
		}
	}
</script>

<style>
	.box-item{
		height: 100px;
		line-height: 100px;
	}
</style>
