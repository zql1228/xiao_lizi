<!-- 首页 -->
<template>
	<view class="content">
		<view class="v-search">
			<u-search placeholder="请输入关键字" v-model="searchval" @custom="search"></u-search>
		</view>	
		<u-swiper indicator :list="list1" radius="0"></u-swiper>
		<u-grid :border="false" 	 col="4">
		    <u-grid-item
		           v-for="(baseListItem,baseListIndex) in baseList"
		           :key="baseListIndex"
			
		    >
		        <u-icon color="#aaaa00" hoverClass="u_icon"
		                :customStyle="{paddingTop:20+'rpx'}"
		                :name="baseListItem.name"
		                :size="49"
		        ></u-icon>
		        <text class="grid-text">{{baseListItem.title}}</text>
		    </u-grid-item>
		</u-grid>
        <u-grid col="2" :border="false" >
            <u-grid-item><text class="text1">领卷专区</text></u-grid-item>
            <u-grid-item><text class="text2">查看更多<u-icon name="play-right-fill" :size="10"></u-icon></text></u-grid-item>
        </u-grid>
       
	</view>
</template>
<script>
	export default {
		data() {
			return {
				searchval:'',
				list1: [
				        'https://cdn.uviewui.com/uview/swiper/swiper1.png',
				        'https://cdn.uviewui.com/uview/swiper/swiper2.png',
				        'https://cdn.uviewui.com/uview/swiper/swiper3.png',
				],
				 baseList: [{
				                    name: 'photo',
				                    title: '签到'
				                    },
				                    {
				                        name: 'lock',
				                        title: '拼团'
				                    },
				                    {
				                        name: 'star',
				                        title: '秒杀'
				                    },
				                    {
				                        name: 'hourglass',
				                        title: '个护'
				                    },
				                    {
				                        name: 'home',
				                        title: '服饰'
				                    },
				                    {
				                        name: 'star',
				                        title: '居家'
				                    },
									{
									    name: 'qq-fill',
									    title: '生鲜'
									},
									{
									    name: 'zhihu-circle-fill',
									    title: '家电'
									},
				                ],
			}
		},
		onLoad() {

		},
		methods: {
			init(){},
			search(){
				
			}
			
		}
	}
</script>

<style lang="scss">
	.v-search{
		padding:16rpx 12rpx;
	}
	.u_icon{
		color: #ffaaff;
	}
    .text1{font-size: 40rpx;}
    .text2{font-size: 24rpx;}

</style>
