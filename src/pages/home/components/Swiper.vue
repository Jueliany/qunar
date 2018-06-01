<template>
	<div class="warpper">
		<swiper :options="swiperOption" >
		    <swiper-slide v-for="item of swiperList"  :key='item.id'>
		    	<img  class="swiper-img" :src="item.imgUrl" >
		    </swiper-slide>
		    
		    <div class="swiper-pagination"  slot="pagination"></div>
	  	</swiper>
  	</div>
</template>
<script>
	export default {
		name:'HomeSwiper',
		data() {
			return {
				swiperOption:{
					pagination: '.swiper-pagination',
					loop:true
				},
				swiperList:[
				{id:'0001',imgUrl:'http://img1.qunarzz.com/piao/fusion/1805/e5/59fad13a64807d02.jpg_750x200_713ae984.jpg'},
				{id:'0002',imgUrl:'http://img1.qunarzz.com/piao/fusion/1805/3b/ef86879aa50e3002.jpg_750x200_2a108508.jpg'}]
			}
		}
		
	}
</script>
<style lang="stylus" scoped>
	.warpper >>> .swiper-pagination-bullet-active
		background: #fff 
	.warpper
		owerflow: hidden
		width: 100%
		padding-boottom: 31.25%		
		.swiper-img
			width: 100%
		
</style>