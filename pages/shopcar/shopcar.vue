<template>
	<view>
		<cu-custom bgColor="bg-gradual-pink" :isBack="true">
			<block slot="backText">返回</block>
			<block slot="content">购物车</block>
		</cu-custom>
		<view class="void">
			<image src='../../static/购物车.png' style='width: 80px; height: 80px; margin:100px 140px 10px;'></image>
			<view class="text-gray" style="margin-left: 110px;">购物车是空的,去逛逛吧</view>
			<navigator url="../home/index" class="text-blue text-shadow" style="margin-left: 160px;">去首页</navigator>
		</view>
		<!-- <checkbox-group class="block" @change="CheckboxChange">
			<view class="manage cu-form-group  flex justify-around bg-white" style="padding:8px 16px;">
				<checkbox class='round' :class="checkbox[0].checked?'checked':''" :checked="checkbox[0].checked?true:false" value="A"></checkbox>
				<view class="margin-left-sm">全选</view>
				<view class="flex-sub text-right text-lg text-black">编辑</view>
			</view>
		</checkbox-group> -->
		
		<!-- <checkbox-group class="block" @change="CheckboxChange">
			<view class="goods">
				<view class="cu-card">
					<view class="cu-item">
						<view class="content flex align-center">
							<checkbox class="round align-center" :class="checkbox[1].checked?'checked':''" :checked="checkbox[1].checked?true:false" value="B"></checkbox>
							<image src="" style="width: 100px; height: 100px;" mode="aspectFill"></image>
							<view>1111</view>
							<view class="computer" style="width: 100px; height: 30px;">
								<button class="text-lg" type="default" style="line-height: 30px;display: inline-block; height: 100%;">+</button>
								<button class="text-lg" type="default" style="display: inline-block; height: 100%;">-</button>
							</view>
						</view>
						<button style="width: 100px; height: 26px; line-height: 26px; display: inline-block;" class="bg-red">立即购买</button>
					</view>
					
				</view>
			</view>
		</checkbox-group> -->
	</view>
</template>

<script>
	export default {
		data() {
			return {
				goodsList: [
					{
						imgSrc: '',
						des: '',
						price: '￥100'
					},
				],
				checkbox: [{
					value: 'A',
					checked: true
				}, {
					value: 'B',
					checked: false
				}, {
					value: 'C',
					checked: false
				}]
			}
		},
		methods: {
			CheckboxChange(e) {
				let items = this.checkbox,
					values = e.detail.value;
				for (let i = 0, lenI = items.length; i < lenI; ++i) {
					items[i].checked = false;
					for (let j = 0, lenJ = values.length; j < lenJ; ++j) {
						if (items[i].value == values[j]) {
							items[i].checked = true;
							break
						}
					}
				}
			}
		}
	}
</script>

<style>

</style>
