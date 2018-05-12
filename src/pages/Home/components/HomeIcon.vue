<template>
  <div class="icon-wrapper">
    <div class="icon-item">
      <img src="../../../assets/imgs/1.png" alt="" class="icon-img">
      <p class="icon-desc">分类</p>
    </div>
    <div class="icon-item">
      <img src="../../../assets/imgs/2.png" alt="" class="icon-img">
      <p class="icon-desc">比赛</p>
    </div>
    <div class="icon-item">
      <img src="../../../assets/imgs/3.png" alt="" class="icon-img">
      <p class="icon-desc">礼包</p>
    </div>
    <div class="icon-item">
      <img src="../../../assets/imgs/4.png" alt="" class="icon-img">
      <p class="icon-desc">成就</p>
    </div>
  </div>
</template>

<script type="text/ecmascript-6">
export default {
  name: 'HomeIcon'
}
</script>

<style lang="stylus" rel="stylesheet/stylus" scoped>
  @import "~@/assets/styles/varibles.styl"
  .icon-wrapper
    height: 1.86rem
    background: $bgColor
    padding: 0 .49688rem 0 .49688rem;
    display: flex
    .icon-item
      flex: 1
      width: 1.11rem
      height: 1.46rem
      position relative
      top: .4rem
      .icon-img
        width: 1rem
        height: 1.08rem
        position: absolute
        top: 0rem
        left: 50%
        transform: translate(-50%,0%)
      .icon-desc
        position:absolute
        top: 72%
        left: 50%
        transform: translateX(-50%)
</style>
