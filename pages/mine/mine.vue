<template>
	<view>
		<cu-custom bgColor="bg-gradual-pink" :isBack="true">
			<block slot="backText">返回</block>
			<block slot="content">我的</block>
		</cu-custom>
		<view class="user-info">
			<view class="padding">
				<navigator url="../userInfo/userInfo" class="cu-avatar round lg" style="background-image: url(../../static/tabbar/_class.png);">
				</navigator>
				<text class="margin text-lg">游客12138</text>
			</view>
			<navigator url="../login/login" class="bg-pink" style="border-radius: 10px; text-align: center; display: inline-block;width: 100px; height: 30px; line-height: 30px;">登录</navigator>
		</view>
		
	</view>
</template>

<script>
	export default {
		data() {
			return {
				
			}
		},
		methods: {
			
		}
	}
</script>

<style scoped>
	.user-info {
		height: 20vh;
		background-color: #fff;
	}
</style>
