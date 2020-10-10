<template>
  <div class="wrapper">
  	<swiper :options="swiperOptions">
	    <swiper-slide v-for="item in banners" :key="item.id">
	    	<img class="swiper-img" :src="item.imgurl">
	    </swiper-slide>
	    <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default{
	name:'HomeSwiper',
	data () {
      return {
      	swiperOptions: {
      	  pagination:'.swiper-pagination'
      	},
      	banners:[{
      		id:'001',
      		imgurl:require('./assets/a.png')
      	},{
      		id:'002',
      		imgurl:require('./assets/b.png')
      	},{
      	},{
      		id:'003',
      		imgurl:require('./assets/c.png')
      	},{
      	}]
      }
	}
}
</script>



<style lang="scss" scoped>
  .wrapper{
  	overflow: hidden;
  	width: 100%;
  	height: 0;
  	padding-bottom:53.2%;
    background: #666;
    .swiper-img{
		width: 100%;
	}
  }
	
</style>