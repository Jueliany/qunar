<template>
	<div >
		<div class="recommend-title">热门推荐</div>
		<ul>
			<li class="item border-bottom" v-for="item of recommendList" :key="item.id">
				<img class="item-img" :src="item.imgUrl">
				<div class="item-info">
					<p class="item-title">{{item.title}}</p>
					<p class="item-desc">{{item.desc}}</p>
					<button class="item-button">查看详情</button>
				</div>			
			</li>
		</ul>
	</div>
	
</template>
<script >
export default{
	name: 'HomeRecommend',
	data () {
		return {
			recommendList:[{
				id:'0001',
				imgUrl:'http://img1.qunarzz.com/sight/p0/1508/2e/d9363ce50a88c8c5ff5a138c67687cd4.water.jpg_200x200_1c15c8f5.jpg',
				title:'深圳野生动物园',
				desc:'中国首批放养式野生动物园之一。'
			},
			{
				id:'0002',
				imgUrl:'http://img1.qunarzz.com/sight/p0/1508/2e/d9363ce50a88c8c5ff5a138c67687cd4.water.jpg_200x200_1c15c8f5.jpg',
				title:'深圳野生动物园',
				desc:'中国首批放养式野生动物园之一。'
			},
			{
				id:'0003',
				imgUrl:'http://img1.qunarzz.com/sight/p0/1508/2e/d9363ce50a88c8c5ff5a138c67687cd4.water.jpg_200x200_1c15c8f5.jpg',
				title:'深圳野生动物园',
				desc:'中国首批放养式野生动物园之一。'
			}
			,{
				id:'0004',
				imgUrl:'http://img1.qunarzz.com/sight/p0/1508/2e/d9363ce50a88c8c5ff5a138c67687cd4.water.jpg_200x200_1c15c8f5.jpg',
				title:'深圳野生动物园',
				desc:'中国首批放养式野生动物园之一。'
			}]
		}
	} 
}
</script>
<style lang="stylus" scoped>
@import '~styles/mixins.styl'
	.recommend-title
		margin-top: .1rem
		line-height: .8rem
		background: #ccc
		text-indent: .2rem
	.item
		overflow: hidden
		display: flex
		height: 1.9rem
		.item-img
			width: 1.7rem
			height: 1.7rem
			padding: .1rem
		.item-info
			flex: 1
			padding: .1rem
			min-width: 0
			.item-title
				line-height:.54rem
				font-size:.32rem
				ellipsis()
			.item-desc
				line-height: .4rem
				color: #ccc
				ellipsis()
			.item-button
				line-height: .44rem
				margin-top: .16rem
				margin-top: .2rem
				background: #FF9300	
				padding: 0 .1rem
				border-radius: .06rem
				color: #fff	
</style>