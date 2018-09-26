<template>
   <div class="search">
     <input type="text" placeholder="请输入搜索城市">
   </div>

</template>

<script>
export default {
  name: 'CitySearch',
 
  data () {
    return {
     
    }
  }
}
</script>


<style lang="less" scoped>
.search{
    height: .72rem;
    padding:0  .1rem;
    background-color:  #00bcd4;
    input{
        box-sizing: border-box;
        padding: 0 .1rem;
        height: .62rem;
        width: 100%;
        line-height: .62rem;
        text-align: center;
    }
}
</style>