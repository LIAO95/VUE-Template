<template>
	<div class="header"> 
      <div class="header-left">
        <div class="iconfont back-icon">&#xe601;</div>
      </div>
      <div class="header-input">
         <span class="iconfont">&#xe628;</span>
      </div>
      <div class="header-right">
         <span class="iconfont arror-icon">&#xe629;</span>
      </div>
	</div>
</template>

<script>
export default{
	name:'HomeHeader'
}
</script>


<style lang="scss" scoped>
.header{
    display: flex;
    height: 4.3rem;
    line-height: 4.3rem;
    background: #00bcb4;
    color: #fff;
   .header-left{
    width:5rem;
    float:left;
    text-align: center;
    .back-icon{
      font-size: 2rem;
    }
   }
   .header-input{
    flex: 1;
    border: 1px solid #fff;
    border-radius: 6px;
    height: 2.8rem;
    line-height: 2.8rem;
    margin-top: 0.7rem;
    padding-left: 1rem;
    color: #ccc;
    }        
    .header-right{
      width:5rem;
      float:right;
      text-align: center;
      .arror-icon{
        font-size: 1rem;
      }
    }
}
        


</style>