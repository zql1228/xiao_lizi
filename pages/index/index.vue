<!-- 首页 -->
<template>
	<view class="content">
		<u-no-network @retry="init"></u-no-network>
		<!-- <shopro-empty v-if="!hasTemplate" :image="$IMG_URL + '/imgs/empty/template_empty.png'" tipText="暂未找到模板，请前往装修~">
		</shopro-empty> -->
		<view class="content">
			<home-head>
				
			</home-head>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				
			}
		},
		onLoad() {

		},
		methods: {
			init(){}
			
		}
	}
</script>

<style lang="scss">
	

</style>
