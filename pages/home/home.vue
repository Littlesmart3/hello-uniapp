<template>
	<view>
		<view>数据绑定的学习</view>
		<view>{{msg}}</view>
		<view>{{'你好' + '世界'}}</view>
		<view>{{1+1}}</view>
		<view>{{flag?"这是假的":"这是真的"}}</view>
		<image :src="imgUrl"></image>
		<view v-for="(item,index) in arr" :key="item.id">
			No.{{index +1}},名字：{{item.name}}, 年龄{{item.age}}
		</view>
		<button type="primary" @click='btn(20)'>按钮</button>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				msg: 'hello',
				flag: false,
				imgUrl: 'http://destiny001.gitee.io/image/monkey_02.jpg',
				arr: [{
					name: '张三',
					age: '22',
					id: 1
				}, {
					name: '李四',
					age: '33',
					id: 2
				}, {
					name: '王五',
					age: '44',
					id: 3
				}, {
					name: '赵六',
					age: '55',
					id: 4
				}]
			}

		},
		methods:{
			btn(e) {
				console.log("点击了"+2)
			}
		}
	}
</script>

<style>
</style>
