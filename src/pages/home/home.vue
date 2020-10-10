<template>
	<div>
	  <home-header></home-header>
	  <home-swiper></home-swiper>
	  <div>test</div>
	</div>
</template>

<script>
import HomeHeader from './components/header.vue'
import HomeSwiper from './components/swiper.vue'
export default{
	name:'home',
	components:{
		HomeHeader:HomeHeader,
		HomeSwiper
	}
}
</script>

<style>
	
</style>