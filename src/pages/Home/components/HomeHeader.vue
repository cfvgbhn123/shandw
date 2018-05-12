<template>
  <div class="wrapper">
    <div class="userIcon">
      <img class="user-img" src="../../../assets/imgs/download.png" alt="userIcon">
    </div>
    <div class="gold">
      <div class="gold-wrap"><span class="gold-num">0</span></div>
    </div>
    <div class="iconfont searchIcon">&#xe632;</div>
    <div class="downloadWrap">
      <img class="downloadIcon" src="../../../assets/imgs/app.png" alt="app">
    </div>
  </div>
</template>

<script type="text/ecmascript-6">
export default {
  name: 'HomeHeader'
}
</script>

<style lang="stylus" rel="stylesheet/stylus" scoped>
  @import "~@/assets/styles/varibles.styl"
  .wrapper
    position relative
    background: $bgColor
    height: 1.2rem
    .userIcon
      width: .7726rem
      height: .7726rem
      position absolute
      border-radius: 50%
      overflow: hidden
      left: .26rem
      top: .2rem
      .user-img
        width: 100%
        height: 100%
    .gold
      height: .4416rem
      width: .3rem
      position: absolute
      left: 1.3rem
      top: .36rem
      .gold-wrap
        position absolute
        top: 0
        left: 0
        display: inline-block
        height: .4416rem
        width: 1rem
        background: rgba(255,255,255,.34)
        border-radius: .2208rem
        color: #ff9000
        text-indent: .6rem
        line-height: .4416rem
      &:before
          content: ""
          display inline-block
          width: .4416rem
          height: .4416rem
          top: 0
          left: 0
          background: url("../../../assets/imgs/gold.png")
          background-size: 100%
  .searchIcon
    height: 1.2rem
    ling-height: 1.2rem
    width:  1rem
    position: absolute
    right: 1.3rem
    box-sizing border-box
    padding-top: .3rem
    font-size: .6rem
    text-align: center
    color: #ffffff
  .downloadWrap
    width: .6rem
    height: .6rem
    position absolute
    top: .28rem
    right: .52rem
    .downloadIcon
      width: 100%
      height: 100%
</style>
