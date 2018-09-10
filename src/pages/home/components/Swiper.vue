<template>
  <div class="wrapper">
      <swiper :options="swiperOption" >
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
  data() {
    return {
        swiperOption:{
            pagination:{
                el:'.swiper-pagination'//以组件的形式展示
            },
            slidesPerView:1,//默认首页
            autoplay:{//自动切换事件
                delay:1000,
                disableOnInteraction:false//操作swiper以后不停止切换插件
            },
            loop:true//无缝轮播
        },
        swiperList:[{
            id:'0001',
            imgurl:'http://img0.imgtn.bdimg.com/it/u=2094405861,3770890021&fm=26&gp=0.jpg'
        },{
            id:'0002',
            imgurl:'http://img1.imgtn.bdimg.com/it/u=645703579,3207914544&fm=26&gp=0.jpg'
        }]
      
    };
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