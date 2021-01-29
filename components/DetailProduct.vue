<template>
	<view>
		<view class="cu-card case" v-for="(detailItem, index) in detailInfo" :key="index">
			<navigator url="../pages/productionDetail/productionDetail" class="cu-item shadow">
				<view class="image">
					<image :src="detailInfo[index].imgSrc" mode="aspectFill"></image>
					<view class="cu-tag bg-gradual-red">超级优惠</view>
					<view class="cu-bar bg-shadeBottom text-bold text-lg"> <text class="text-cut">{{detailInfo[index].des}}</text></view>
				</view>
				<view class="cu-list">
					<view class="cu-item flex" style="margin: 10px 0 0 0;">
						<text class="text-red flex-sub text-center" style="font-size: 18px; font-weight: 600;">{{detailInfo[index].price}}</text>
						<view class="content flex margin-left" style="width: 200px;">
							<button class="cu-btn bg-red flex-sub">加入购物车</button>
							<button class="cu-btn line-red flex-sub margin-left">预定</button>
						</view>
					</view>
				</view>
			</navigator>
		</view>
	</view>
</template>

<script>
	export default {
		name: 'DetailProduct',
		props:['detailInfo'],
		data() {
			return {
				
			}
		},
		methods: {
			
		}
	}
</script>

<style>

</style>
