<template>
	<view>
		<!-- <view>
			<text>我会唱跳Rap篮球</text>
		</view>
		<view>
			<text selectable>我会唱跳Rap篮球</text>
		</view>
		<view>
			<text selectable space="ensp">我会    唱跳Rap篮球</text>
		</view>
		<view>
			<text selectable space="emsp">我会    唱跳Rap篮球</text>
		</view>
		<view>
			<text selectable space="nbsp" style="font-size: 100px;">我会    唱跳Rap篮球</text>
		</view>
		<view>
			<text>&amp;</text>
		</view> -->
		<view class="box2" hover-class="box2-active">
			<view class="box" :hover-start-time="2000" :hover-stay-time="2000" hover-class="box-active"
				hover-stop-propagation>
				我是一个大盒子
			</view>
		</view>
		<button>按钮</button>
		<button size="mini">按钮</button>
		<button type="primary">按钮</button>
		<button type="primary" plain>按钮</button>
		<button type="primary" disabled>按钮</button>
		<button type="primary" loading>按钮</button>
		<image src="http://destiny001.gitee.io/image/cxk.gif"></image>
	<image src="http://destiny001.gitee.io/image/cxk.gif" mode="aspectFit"></image>
	<image src="http://destiny001.gitee.io/image/cxk.gif" mode="aspectFill"></image>
	</view>
</template>

<script>
</script>

<style>
	.box {
		display: flex;
		justify-content: center;
		align-items: center;
		width: 100px;
		height: 100px;
		background: green;
	}

	.box2 {
		display: flex;
		justify-content: center;
		align-items: center;
		width: 200px;
		height: 200px;
		background-color: #007AFF;
	}

	.box-active {
		background: red;
	}

	.box2-active {
		background: pink;
	}
</style>
