<template>
  <div class="wrapper">
      <swiper v-if="swiperList.length>1" :options="swiperOption" >
         <!-- slides -->
        <swiper-slide v-for="item of swiperList" :key="item.id">
            <img class="swiper-img" :src="item.imgurl" alt="">
        </swiper-slide>
        <!-- Optional controls -->
        <div class="swiper-pagination"  slot="pagination"></div><!--小圆点-->
        
    </swiper>
  </div>
</template>

<script>
export default {
  name: "HomeSwiper",
  props:{
      swiperList:Array
  },
  data() {
    return {
        swiperOption:{
            pagination:{
                el:'.swiper-pagination'//以组件的形式展示
            },
            observer:true,//修改swiper自己或子元素时，自动初始化swiper 
　　        observeParents:true,//修改swiper的父元素时，自动初始化swiper 
            loop:true,//无缝轮播   
            slidesPerView:1,//默认首页
            autoplay:{//自动切换事件
                delay:1000,
                disableOnInteraction:false//操作swiper以后不停止切换插件
            },
           
           
        }
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="less" scoped>
.wrapper /deep/ .swiper-pagination-bullet-active{
    background: #fff}

.wrapper{
    overflow: hidden;
    width: 100%;
    height: 0;
    padding-bottom:32.5%;
   .swiper-img{
        width: 100%;
    }


    
    
}
</style>