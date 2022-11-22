<template>
	<view>
		<u-navbar title="电子学生证" :autoBack="true" bgColor="#fff" placeholder>
			<view class="u-nav-slot" slot="right">
				关闭
			</view>
		</u-navbar>
		<view class="content">
			<view class="top">

			</view>
			<view class="center">
				<view class="circle1"></view>
				<view class="divider"></view>
				<view class="circle2"></view>
			</view>
			<view class="bottom"></view>
		</view>

	</view>
</template>

<script>
	export default {
		data() {
			return {
				title: 'Hello'
			}
		},
		onLoad() {

		},
		methods: {

		}
	}
</script>

<style lang="scss" scoped>
	.content {
		height: calc(100vh - 44px);
		background-color: #f6f7fb;
		padding: 4%;

		.top {
			height: 20%;
			background-color: #fff;
			border-radius: 5px 5px 0 0;
			border: 1px solid #fffffd;
		}

		.center {
			position: relative;
			margin-top: 0.3%;
			height: 3%;
			background-color: #fff;
			display: flex;
			flex-flow: column;
			justify-content: center;
			overflow: hidden;

			.circle1 {
				position: absolute;
				top: 0;
				left: -15rpx;
				width: 30rpx;
				height: 100%;
				border-radius: 50%;
				background-color: #f6f7fb;
			}

			.divider {
				background: none;
				border-color: #f7f7f7;
				border-style: dotted none none none;
				border-width: 4.5px;
			}

			.circle2 {
				position: absolute;
				top: 0;
				right: -15rpx;
				width: 100rpx;
				height: 100%;
				border-radius: 60rpx;
				background-color: #f6f7fb;
			}

		}
		.bottom{
			height: 55%;
			background-color: #fff;
		}

	}
</style>
