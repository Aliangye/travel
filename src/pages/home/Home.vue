<template>
  <div>
    <home-header></home-header>
    <home-swiper></home-swiper>
    <home-icons></home-icons>
     <home-recment></home-recment>
    
  </div>
</template>

<script>
import HomeHeader from './components/Header'
import HomeSwiper from './components/Swiper'
import HomeIcons from './components/Icons'
import HomeRecment from './components/Recment'
export default {
  name: 'Home',
  data () {
    return {
    }
  },
  components: {
  HomeHeader,
  HomeSwiper,
  HomeIcons,
  HomeRecment,
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="less" scoped>
</style>
