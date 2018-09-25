<template>
  <div class="recment">
    <div class="recment-title">热销景点</div>
    <div class="item" v-for="recment of recmentList" :key="recment.id">
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
  name: "HomeRecment",
  props:{
      recmentList:Array
  },
  data() {
     return {
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
    height: 1.88rem;
    display: flex;
    border-bottom: 1px solid #ccc;
    .item-img{
        width:30%;
        height: 100%;
        img{
            width: 100%;
            height: 100%;
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
            padding: 0 .2rem;
            color: #fff;
        }
    }
}
</style>