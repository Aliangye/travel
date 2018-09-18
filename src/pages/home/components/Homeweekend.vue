<template>
  <div class="recment">
    <div class="recment-title">周末旅行</div>
    <div class="item" v-for="recment of weekendList" :key="recment.id">
        <div class="item-img">
            <img :src="recment.imgurl" alt="">
        </div>
        <div class="item-info">
            <p class="info-name">{{recment.infoname}}</p>
            <p class="info-txt">{{recment.infotxt}}</p>
            <button class="info-detail">查看详情</button>
        </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "HomeWeekend",
  data() {
     return {
         weekendList:[{
             id:'0001',
             imgurl:'https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1536773092132&di=89acfe6a30619fb630af2806936b3ce0&imgtype=0&src=http%3A%2F%2Fimg1.qunarzz.com%2Ftravel%2Fpoi%2F1412%2Fc7%2Fc7fd4260b404a712cdb.jpg_r_1024x683x95_4d60305a.jpg',
             infoname:'云南佛塔',
             infotxt:'世界上最大的祈福圣地'
         },
         {
             id:'0002',
             imgurl:'https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1536773092131&di=3c3423e12e9f35bac6523fefb0bced87&imgtype=0&src=http%3A%2F%2Fpic7.nipic.com%2F20100428%2F1628220_133031011465_2.jpg',
             infoname:'普吉岛',
             infotxt:'热情如火的泰国清凉之旅'
         },{
             id:'0003',
             imgurl:'https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1536773092129&di=c0f33f4dd62b7b341f0cdcd78fd0bb3c&imgtype=0&src=http%3A%2F%2Fimg1.qunarzz.com%2Ftravel%2Fpoi%2F1408%2F20%2Ffee32bf45b8d97c0ffffffffc8d65eac.jpg_r_1024x683x95_1e3e5895.jpg',
             infoname:'马尔代夫',
             infotxt:'甜蜜浪漫的情侣度假之地'
         },{
             id:'0004',
             imgurl:'https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1536773092129&di=c0f33f4dd62b7b341f0cdcd78fd0bb3c&imgtype=0&src=http%3A%2F%2Fimg1.qunarzz.com%2Ftravel%2Fpoi%2F1408%2F20%2Ffee32bf45b8d97c0ffffffffc8d65eac.jpg_r_1024x683x95_1e3e5895.jpg',
             infoname:'马尔代夫',
             infotxt:'甜蜜浪漫的情侣度假之地'
         },{
             id:'0005',
             imgurl:'https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1536773092129&di=c0f33f4dd62b7b341f0cdcd78fd0bb3c&imgtype=0&src=http%3A%2F%2Fimg1.qunarzz.com%2Ftravel%2Fpoi%2F1408%2F20%2Ffee32bf45b8d97c0ffffffffc8d65eac.jpg_r_1024x683x95_1e3e5895.jpg',
             infoname:'马尔代夫',
             infotxt:'甜蜜浪漫的情侣度假之地'
         }]
        }
    }
}   
</script>

<style lang="less" scoped>
.recment-title{
    background-color: #ccc;
    width:100%;
    height: .44rem;
    line-height: .44rem;
    color: #000;
    padding-left: .10rem;
}
.item{
    overflow: hidden;
    width: 100%;
    border-bottom: 1px solid #ccc;
    .item-img{
        width:100%;
        height: 0;
        padding-bottom: 35%;
        overflow: hidden;
        img{
            width: 100%;
        }
    }
    .item-info{
        flex: 1;
        padding-left: .1rem;
        .info-name{
            font-size: .34rem;
            line-height: .54rem;
            color: #000;
        }
        .info-txt{
            font-size: .28rem;
            line-height: .54rem;
        }
        .info-detail{
            margin-top: 0.25rem;
            border-radius: .06rem;
            background-color: #ff9300;
            padding-bottom: 0 .2rem;
            margin-bottom: .1rem;
            color: #fff;
        }
    }
}
</style>