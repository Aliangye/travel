<template>
   <div class="header">
       城市选择
        <router-link to="/">
            <div class="header-back">返回</div>
        </router-link>
   </div>

</template>

<script>
export default {
  name: 'CityHeader',
 
  data () {
    return {
     
    }
  }
}
</script>


<style lang="less" scoped>
.header{
    position: relative;
    overflow: hidden;
    height: .86rem;
    line-height: .86rem;
    text-align: center;
    color: #fff;
    background-color: #00bcd4;
    font-size: .32rem;
    .header-back{
        position: absolute;
        top: 0;
        left: 0;
        width: .64rem;
        font-size: .32rem;
        text-align: center;
        color: #fff;
    }
}
</style>