<template>
  <div class="recommend-wrapper">
    <div class="show-list">
      <span class="item title">
        <span class="icon"></span>
        每日推荐
      </span>
      <span class="item">
        <span class="icon" v-show="false"></span>
          小游戏
      </span>
      <span class="item">
        <span class="icon" v-show="false"></span>
          新游新服
      </span>
      <span class="item">
        <span class="icon" v-show="false"></span>
        闪电咨询
      </span>
    </div>
    <div class="arrowIcon" @click="change">
      <img class="down" src="../../../assets/imgs/arrow.png" v-show="!flag"/>
      <img class="up" src="../../../assets/imgs/arrow.png" v-show="flag"/>
    </div>
    <div class="hidden-list" v-show="flag">
      <span class="item">
        <span class="icon" v-show="false"></span>
        全部游戏
      </span>
    </div>
  </div>
</template>

<script type="text/ecmascript-6">
export default {
  name: 'HomeRecommend',
  data () {
    return {
      flag: false
    }
  },
  methods: {
    change () {
      this.flag = !this.flag
    }
  }
}
</script>

<style lang="stylus" rel="stylesheet/stylus" scoped>
  @import "~@/assets/styles/varibles.styl"
  .recommend-wrapper
    width:100%
    height: 1rem
    position relative
    font-size: .3rem
    background: $bgColor
    .show-list
      margin: 0 .49688rem 0 .49688rem;
      display: flex
      height: .9934rem
      line-height: .9934rem
      justify-content space-around
      .item
        display: inline-block
        color: #cccccc
        position relative
      .title
        color: #ffffff
        .icon
          display: block
          width: .24rem
          height: .26rem
          background-image: url('../../../assets/imgs/recommend.png')
          background-size: 100%
          position: absolute
          top: 50%
          left: 0
          transform: translate(-100%, -50%)
    .arrowIcon
        width: .3139rem
        position: absolute
        top: 0.2rem
        right: .2rem
        .down
          position: absolute
          display: block
          width:.3rem
          height: .2rem
          top: .18rem
          left: 0
        .up
          position: absolute
          display: block
          width:.3rem
          height: .2rem
          top: .18rem
          left: 0
          transform: rotate(180deg)
    .hidden-list
      position: absolute
      padding-left: .4rem
      height: .9934rem
      width: 100%
      line-height: .9934rem
      background: $bgColor
      z-index : 999
      .item
        display: inline-block
        color: #cccccc
        width: 25%
        text-align: center
</style>
