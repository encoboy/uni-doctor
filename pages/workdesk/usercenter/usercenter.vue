<template>
	<view class="hospital-box" :style="{ height: windowHeight + 'px' }">
		<view class="header-img-box">
			<image src="@/static/img/title-img.png" mode="aspectFit"></image>
		</view>
		<view class="header-big-title">
			个人中心
		</view>
		<view class="userInfo-box">
			<view class="username">
				胡 克
			</view>
			<view class="userimg">
				<image src="../../../static/img/head-photo.png" mode="aspectFit"></image>
			</view>
			<view class="workname">
				职称：慢性疾病专家
			</view>
			<view class="long-btn editInfo" @click="goChangeDoctorInfo">
				修改信息
			</view>
			<view class="long-btn changeAccount">
				切换账号
			</view>
			<view class="long-btn exit">
				退出登录
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				windowHeight:0,
			}
		},
		onLoad() {
			const res = uni.getSystemInfoSync();
			this.windowHeight = res.windowHeight;
		},
		methods:{
			goChangeDoctorInfo(){
				uni.navigateTo({
					url:'/pages/workdesk/usercenter/changedoctorInfo/changedoctorInfo'
				})
			}
		}
	}
</script>

<style lang="scss">
	.hospital-box{
		.userInfo-box{
			flex: 7.5;
			flex-basis: 0;
			background-color: #d7f7f7;
			margin-bottom: 20rpx;
			display: flex;
			flex-direction: column;
			align-items: center;
			.username{
				color: blue;
				font-size: 40rpx;
				margin: 20rpx 0;
			}
			.userimg{
				margin: 20rpx 0;
				image{
					width: 200rpx;
					height: 200rpx;
				}
			}
			.workname {
				font-size: 30rpx;
				margin: 20rpx 0;
			}
			.editInfo,.changeAccount,.exit{
				margin:20rpx 0;
			}
		}
	}
</style>
