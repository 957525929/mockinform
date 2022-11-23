<template>
	<view class="page">
		<u-navbar title="电子学生证" :autoBack="true" bgColor="#fff" placeholder>
			<view class="u-nav-slot" slot="right">
				关闭
			</view>
		</u-navbar>
		<view class="content">
			<view class="top">
				<view class="head">
					<image src="../../static/wpx.jpg"></image>
				</view>

				<view class="top-right">
					<view
						style="display: flex;align-items: center; width: 80%;height: 50rpx;border-bottom: 1.2px solid #eeeeee;padding-bottom: 8rpx;">
						<view style="font-size: 40rpx;font-weight: 700;margin-right: 30rpx;">学生证</view>
						<view style="width: 58%;height: 85%;">
							<image style="width: 100%;height:100%;" src="../../static/title.png"></image>
						</view>
					</view>
					<view style="display: flex;margin-top: 15rpx;">
						<view style="color: #2d2d2d;font-size: 28rpx;font-weight: 550">姓名：</view>
						<view style="color: #777777;font-size: 28rpx">王鹏翔</view>
					</view>
					<view style="display: flex;margin-top: 10rpx;">
						<view style="color: #2d2d2d;font-size: 28rpx;font-weight: 550">学号：</view>
						<view style="color: #777777;font-size: 28rpx">172031227</view>
					</view>
					<view style="display: flex;margin-top: 10rpx;">
						<view style="color: #2d2d2d;font-size: 28rpx;font-weight: 550">院系：</view>
						<view style="color: #777777;font-size: 28rpx">美术与设计学院</view>
					</view>
					<view style="display: flex;margin-top: 30rpx;">
						<view style="color: #2d2d2d;font-size:28rpx;font-weight: 550">班级：</view>
						<view style="color: #777777;font-size: 28rpx">1班</view>
					</view>
				</view>
			</view>
			<view class="center">
				<view class="circle1"></view>
				<view class="divider"></view>
				<view class="circle2"></view>
			</view>
			<view class="bottom">
				<view style="display: flex;justify-content: space-between;padding: 1%;" v-for="item in infrom"
					:key='item.label'>
					<view style="color: #8f8f8f;font-size: 28rpx">{{item.label}}</view>
					<view :style="{color:item.color?item.color:'#000',fontSize:'28rpx'}">{{item.value}}</view>
				</view>
				<view style="display: flex;justify-content: center;">
					<view class="status">
						<image style="height: 100%;width: 100%;" src="../../static/status.png"></image>
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
				title: 'Hello',
				infrom: [{
						label: '性别',
						value: '男'
					},
					{
						label: '宿舍范围',
						value: '校外',
						color: '#f0fe64'
					},
					{
						label: '宿舍楼',
						value: '27栋',
						color: '#f0fe64'
					},
					{
						label: '宿舍',
						value: '802A',
						color: '#f0fe64'
					},
					{
						label: '手机号码',
						value: '13067301362'
					},
					{
						label: '专业',
						value: '工艺美术品设计'
					},
					{
						label: '专业方向',
						value: '漆艺方向'
					},
					{
						label: '学制',
						value: ''
					},
					{
						label: '入学年份',
						value: '2021.0'
					},
					{
						label: '辅导员',
						value: '周方圆'
					},
					{
						label: '辅导员手机号码',
						value: '15005068899'
					}
				]
			}
		},
		onLoad() {

		},
		methods: {

		}
	}
</script>

<style lang="scss" scoped>
	.page {
		height: 100vh;
		background-color: #f6f7fb;

		.content {
			height: 88%;
			background-color: #f6f7fb;
			padding: 4%;

			.top {
				display: flex;
				height: 23%;
				background-color: #fff;
				border-radius: 5px 5px 0 0;
				border: 1px solid #fffffd;

				.head {
					display: flex;
					height: 100%;
					flex: 1;
					width: 0;
					justify-content: center;
					align-items: center;

					image {
						height: 80%;
						width: 80%;
						border-radius: 10rpx 10rpx 20rpx 20rpx;
					}
				}

				.top-right {
					flex: 2;
					width: 0;
					padding-top: 5%;

				}
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

			.bottom {
				position: relative;
				height: 60%;
				background-color: #fff;
				padding: 5% 3%;

				.status {
					position: absolute;
					bottom: 2%;
					width: 450rpx;
					height: 300rpx;
				}
			}

		}
	}
</style>
