<template>
	<div class="icons">
		<swiper>
			<swiper-slide v-for="(page,index) in pages" :key="index">
				<div 
				class="icon" 
				v-for="item in page"
				:key="item.id"
				>
					<div class="icon-img">
						<img class="icon-img-content" :src="item.imgurl" >
					</div>
					<p class="icon-desc">{{item.desc}}</p>
				</div>
            </swiper-slide>
        </swiper>

		
	</div>
</template>
<script>
export default{
	name:'HomeIcons',
	data () {
	  return {
		iconList: [{
		  id:'001',
	      imgurl:'https://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20209/158387fe5376294f3776d01358d6b73b.png',
	      desc:'热门景点1'
		},{
		  id:'002',
	      imgurl:'https://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20209/158387fe5376294f3776d01358d6b73b.png',
	      desc:'热门景点2'
		},{
		  id:'003',
	      imgurl:'https://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20209/158387fe5376294f3776d01358d6b73b.png',
	      desc:'热门景点3'
		},{
		  id:'004',
	      imgurl:'https://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20209/158387fe5376294f3776d01358d6b73b.png',
	      desc:'热门景点4'
		},{
		  id:'005',
	      imgurl:'https://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20209/158387fe5376294f3776d01358d6b73b.png',
	      desc:'热门景点3'
		},{
		  id:'006',
	      imgurl:'https://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20209/158387fe5376294f3776d01358d6b73b.png',
	      desc:'热门景点3'
		},{
		  id:'007',
	      imgurl:'https://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20209/158387fe5376294f3776d01358d6b73b.png',
	      desc:'热门景点3'
		},{
		  id:'008',
	      imgurl:'https://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20209/158387fe5376294f3776d01358d6b73b.png',
	      desc:'热门景点3'
		},{
		  id:'009',
	      imgurl:'https://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20209/158387fe5376294f3776d01358d6b73b.png',
	      desc:'热门景点9'
		}]
	   }

	},
	computed: {
		pages () {
			const pages = []
			this.iconList.forEach((item, index) => {
				const page = Math.floor(index / 8)
				if (!pages[page]) {
					pages[page] = []
				}
				pages[page].push(item)
			})
			return pages
		}
	}

}	
</script>
<style lang="scss" scoped>
.icons >>> .swiper-container{
	overflow: hidden;
	height: 0;
	padding-bottom: 50%;
}
.icon{
	position:relative;
	overflow: hidden;
	width: 25%;
	float: left;
	height: 0;
	padding-bottom: 25%;
	.icon-img{
		position: absolute;
		left:0;
		right:0;
		top: 0;
		bottom:2rem;
		box-sizing: border-box;
		padding: 0.5rem;
		.icon-img-content{
		height: 100%;
		display: block;
        margin: 0 auto;
	    }
	}
	.icon-desc{
		position: absolute;
		left:0;
		right:0;
		bottom:1rem;
		text-align: center;
	}

	
}


</style>