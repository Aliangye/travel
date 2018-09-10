<template>
  <div class="wrapper">
      <div class="icons-img" v-for="icon of iconsList" :key="icon.id">
          <div class="icon-img">
              <img :src="icon.imgurl" alt="">
          </div>
          <p>{{icon.icontxt}}</p>
      </div>

  </div>
</template>

<script>
export default {
  name: "HomeIcons",
  data() {
    return {
        iconsList:[{
            id:'1',
            imgurl:'https://s.qunarzz.com/package_mobile/app/outbround/play_v2.png',
            icontxt:'旅游景点'
        },{
            id:'2',
            imgurl:'https://s.qunarzz.com/package_mobile/app/outbround/play_v2.png',
            icontxt:'自助服务'
        },
        {
            id:'3',
            imgurl:'https://s.qunarzz.com/package_mobile/app/outbround/play_v2.png',
            icontxt:'自助服务'
        },{
            id:'4',
            imgurl:'https://s.qunarzz.com/package_mobile/app/outbround/play_v2.png',
            icontxt:'自助服务'
        },{
            id:'5',
            imgurl:'https://s.qunarzz.com/package_mobile/app/outbround/play_v2.png',
            icontxt:'自助服务'
        },{
            id:'6',
            imgurl:'https://s.qunarzz.com/package_mobile/app/outbround/play_v2.png',
            icontxt:'自助服务'
        },{
            id:'7',
            imgurl:'https://s.qunarzz.com/package_mobile/app/outbround/play_v2.png',
            icontxt:'自助服务'
        },{
            id:'8',
            imgurl:'https://s.qunarzz.com/package_mobile/app/outbround/play_v2.png',
            icontxt:'自助服务'
        }]
      
    }
  }
};
</script>

<style lang="less" scoped>
.wrapper{
    overflow: hidden;
    width: 100%;
    height: 0;
    padding-bottom:50%;
    .icons-img{
        position: relative;
        float: left;
        width: 25%;
        height: 0;
        padding-bottom:25%;
        .icon-img{
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0.44rem;
            margin: 5%;
            background: pink;
            border-radius: 25%;
        }
            img{
                display: block;
                height: 100%;
                margin: 0 auto;
            }
        p{
            position: absolute;
            left: 0;
            right: 0;
            bottom: 0;
            line-height: .44rem;
            text-align: center;
        }
    }

}


    
    

</style>