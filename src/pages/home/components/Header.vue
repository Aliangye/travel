<template>
  <div class="header">
    <div class="header-left">放回</div>
    <div class="header-input">
        <input type="text" placeholder="搜索去哪里">
    </div>
    <div class="header-right">{{this.city}}</div>
  </div>
</template>

<script>
export default {
  name: 'HomeHeader',
  props:{
      city:String
  },
  data () {
    return {
      msg: ''
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="less" scoped>
.header{
    display: flex;
    color: #fff;
    background-color: #00bcd4;
    line-height: .86rem;//在初始化中设置的html像素是50px，苹果手机的像素点是2个
    .header-left{
        width: .64rem;
        float: left;
    }
    .header-input{
        flex-grow: 1;
        margin-left: .2rem;
        input{
            width: 100%;
            height: .64rem;
            line-height: .64rem;
            border-radius: 0.1rem;
        }
    }
    .header-right{
        width: 1.24rem;
        float: right;
        text-align: center;
    }
}
</style>