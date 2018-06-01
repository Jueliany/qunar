<template>
	<div class="icons">
		<swiper >
			<swiper-slide  v-for="(page,index) of pages" :key="index" >
				<div class="icon" v-for="item of page" :key="item.id">
					<div class="icon-img">
						<img class="icon-img-content" :src="item.url" />
					</div>
					<p class="icon-desc">{{item.title}}</p>
				</div>	
			</swiper-slide>			
		</swiper>	
	</div>	
</template>

<script>
export default {
	name: 'HomeIcons',
	data () {
		return {
			iconList: [{
				          title: '景点门票景点门票',
				          id: 1,
				          url: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png'
				        },
				        {
				          title: '踏青赏花',
				          id: 2,
				          url: 'http://img1.qunarzz.com/piao/fusion/1803/bd/9f7b9b2b60c1502.png'
				        },
				        {
				          title: 'Q+精选',
				          id: 3,
				          url: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png'
				        },
				        {
				          title: '景点门票',
				          id: 4,
				          url: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png'
				        },
				        {
				          title: '踏青赏花',
				          id: 5,
				          url: 'http://img1.qunarzz.com/piao/fusion/1803/bd/9f7b9b2b60c1502.png'
				        },
				        {
				          title: '景点门票',
				          id: 6,
				          url: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png'
				        },
				        {
				          title: '踏青赏花',
				          id: 7,
				          url: 'http://img1.qunarzz.com/piao/fusion/1803/bd/9f7b9b2b60c1502.png'
				        },
				        {
				          title: '景点门票',
				          id: 8,
				          url: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png'
				        },
				        {
				          title: '景点门票',
				          id: 9,
				          url: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png'
				        },
				        {
				          title: '景点门票',
				          id: 10,
				          url: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png'
				        },
				        {
				          title: '景点门票',
				          id: 11,
				          url: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png'
				        },
				        {
				          title: '踏青赏花',
				          id: 12,
				          url: 'http://img1.qunarzz.com/piao/fusion/1803/bd/9f7b9b2b60c1502.png'
				        },
				        {
				          title: 'Q+精选',
				          id: 13,
				          url: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png'
				        },
				        {
				          title: '景点门票',
				          id: 14,
				          url: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png'
				        },
				        {
				          title: '踏青赏花',
				          id: 15,
				          url: 'http://img1.qunarzz.com/piao/fusion/1803/bd/9f7b9b2b60c1502.png'
				        },
				        {
				          title: '景点门票',
				          id: 16,
				          url: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png'
				        }
				      ]
		}
	},
	computed: {
		pages () {
			const pages = []
			this.iconList.forEach((item,index) =>{
				const page=Math.floor(index/8)
				if(!pages[page]){
					pages[page] = []
				}
				pages[page].push(item)
			})
			return pages
		}
	}

}
</script>

<style lang="stylus" scoped>
	@import '~styles/varibles.styl'
	@import '~styles/mixins.styl'
	.icons >>> .swiper-container
		height:0
		padding-bottom: 50%
	.icon
		position: relative
		overflow: hidden
		float:left
		width: 25%;
		padding-bottom: 25%
		height: 0;
		.icon-desc
			position: absolute
			left: 0
			right: 0
			bottom: 0
			line-height: .44rem
			color: $darkTextColor
			text-align: center
			ellipsis()
		.icon-img
			position: absolute
			top: 0
			left: 0
			right: 0
			bottom: .44rem
			box-sizing: border-box
			padding:.1rem
			.icon-img-content					
				display: block					
				margin: 0 auto
				height: 100%
			
		
</style>