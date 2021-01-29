<template>
	<view>
		<cu-custom bgColor="bg-gradual-pink">
			<block slot="content">首页</block>
		</cu-custom>
		<scroll-view scroll-x class="bg-white nav">
			<view class="flex text-center">
				<view class="cu-item flex-sub" :class="index==TabCur?'text-pink cur':''" v-for="(item,index) in detailTitle" :key="index"
				 @tap="tabSelect" :data-id="index">
					{{item}}
				</view>
			</view>
		</scroll-view>
		<view v-show="TabCur=== '0'">
			<DetailProduct :detailInfo = "detailInfo"></DetailProduct>
		</view>
	</view>
</template>

<script>
	import DetailProduct from '../../components/DetailProduct.vue'
	export default {
		components: {
			DetailProduct
		},
		data() {
			return {
				TabCur: '0',
				scrollLeft: 0,
				detailTitle: ['宠物疫苗', '宠物美容', '宠物用品', '关于我们'],
				detailInfo: [
					{
						imgSrc: 'https://dss3.bdstatic.com/70cFv8Sh_Q1YnxGkpoWK1HF6hhy/it/u=1555752930,3662488675&fm=26&gp=0.jpg',
						des: '成年狗疫苗',
						price: '￥100'
					},
					{
						imgSrc: 'https://dss3.bdstatic.com/70cFv8Sh_Q1YnxGkpoWK1HF6hhy/it/u=1555752930,3662488675&fm=26&gp=0.jpg',
						des: '成年狗疫苗',
						price: '￥100'
					},
					{
						imgSrc: 'https://dss3.bdstatic.com/70cFv8Sh_Q1YnxGkpoWK1HF6hhy/it/u=1555752930,3662488675&fm=26&gp=0.jpg',
						des: '成年狗疫苗',
						price: '￥100'
					}
				]	
			}
		},
		methods: {
			tabSelect(e) {
				this.TabCur = e.currentTarget.dataset.id;
				this.scrollLeft = (e.currentTarget.dataset.id - 1) * 60
			}
		}
	}
</script>

<style scoped>
	.cu-list {
		height: 40px;
	}

	.cuIcon-cartfill {
		font-size: 24px;
		margin: 10px;
	}
</style>
