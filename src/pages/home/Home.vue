<template>
  <div>
    <home-header :city="city"></home-header>
    <home-swiper :swiperList="swiperList"></home-swiper>
    <home-icons></home-icons>
    <home-recment :recmentList="recmentList"></home-recment>
    <home-weekend :recmentList="recmentList"></home-weekend>
  </div>
</template>

<script>
import HomeHeader from './components/Header'
import HomeSwiper from './components/Swiper'
import HomeIcons from './components/Icons'
import HomeRecment from './components/Recment'
import HomeWeekend from './components/Homeweekend'
import axios from 'axios'//引入axios组件
export default {
  name: 'Home',
  data () {
    return {
      city:'',
      recmentList:[],
      swiperList:[]
    }
  },
  components: {
  HomeHeader,
  HomeSwiper,
  HomeIcons,
  HomeRecment,
  HomeWeekend,
  },
  methods:{
    getHomeInfo(){
      axios.get('/api/index.json')
        .then(this.getHomeInfoSucc)
    },
    getHomeInfoSucc(res){
      res = res.data
      if(res.ret && res.data){
        const data = res.data
        this.city = data.city
        this.recmentList = data.recmentList
        this.swiperList = data.swiperList
      }
    console.log(res)
    }
  },
  mounted () {//生命周期函数  在页面加载之前发送axios请求
    this.getHomeInfo()
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="less" scoped>
</style>
