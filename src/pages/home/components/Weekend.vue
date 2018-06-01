<template>
	<div >
		<div class="title">周末去哪</div>
		<ul>
			<li class="item border-bottom" v-for="item of recommendList" :key="item.id">
				<div class="item-img-wrapper">
					<img class="item-img" :src="item.imgUrl">
				</div>
				<div class="item-info">
					<p class="item-title">{{item.title}}</p>
					<p class="item-desc">{{item.desc}}</p>
				</div>			
			</li>
		</ul>
	</div>
	
</template>
<script >
export default{
	name: 'HomeWeekend',
	data () {
		return {
			recommendList:[{
				id:'0001',
				imgUrl:'http://img1.qunarzz.com/sight/source/1505/fa/ca65fde9677de2.jpg_r_640x214_4500e3ff.jpg',
				title:'深圳野生动物园',
				desc:'中国首批放养式野生动物园之一。'
			},
			{
				id:'0002',
				imgUrl:'http://img1.qunarzz.com/sight/source/1505/fa/ca65fde9677de2.jpg_r_640x214_4500e3ff.jpg',
				title:'深圳野生动物园',
				desc:'中国首批放养式野生动物园之一。'
			},
			{
				id:'0003',
				imgUrl:'http://img1.qunarzz.com/sight/source/1505/fa/ca65fde9677de2.jpg_r_640x214_4500e3ff.jpg',
				title:'深圳野生动物园',
				desc:'中国首批放养式野生动物园之一。'
			}
			,{
				id:'0004',
				imgUrl:'http://img1.qunarzz.com/sight/source/1505/fa/ca65fde9677de2.jpg_r_640x214_4500e3ff.jpg',
				title:'深圳野生动物园',
				desc:'中国首批放养式野生动物园之一。'
			}]
		}
	} 
}
</script>
<style lang="stylus" scoped>
@import '~styles/mixins.styl'
	.title
		margin-top: .1rem
		line-height: .8rem
		background: #ccc
		text-indent: .2rem
	.item-img-wrapper
		height: 0
		overflow: hidden
		padding-bottom: 33.9%
		.item-img		
			width: 100%
	.item-info
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
		
</style>