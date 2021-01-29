<template>
	<view>
		<view class="login bg-white">
			<view class="">登录</view>
			<view class="">LOGIN</view>
			<view class="cu-form-group">
				<view class="title">用户名或手机号：</view>
				<input placeholder="请输入用户名或手机号" name="input"></input>
			</view>
			<view class="cu-form-group">
				<view class="title">登录密码:</view>
				<input placeholder="请输入登录密码" name="password"></input>
			</view>
			<text url="">还没注册，去 <navigator url="../register/register" class="text-blue" style="display: inline-block;">注册</navigator></text>
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
