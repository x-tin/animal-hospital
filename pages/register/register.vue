<template>
	<view>
		<view class="login bg-white">
			<view class="">注册</view>
			<view class="">REGISTER</view>
			<view class="cu-form-group">
				<view class="title">手机号码</view>
				<input placeholder="请输入手机号码" name="input"></input>
				<view class="cu-capsule radius">
					<view class='cu-tag bg-blue '>
						+86
					</view>
					<view class="cu-tag line-blue">
						中国大陆
					</view>
				</view>
			</view>
			<view class="cu-form-group">
				<view class="title">验证码</view>
				<input placeholder="获取验证码" name="input"></input>
				<button class='cu-btn bg-green shadow'>验证码</button>
			</view>
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
.login {
	height: 100vh;
}
</style>

