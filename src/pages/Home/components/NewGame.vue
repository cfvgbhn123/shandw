<template>
  <div class="wrapper">
    <div class="title">
      新游新服
    </div>
    <span class="arrow"></span>
    <div class="banner">
      <div class="img-wrap">
        <div class="tag"></div>
        <img class="img" src="https://open.shandw.com/uploads/fbebac7758fb1e8bd77440f308f2119a.png">
      </div>
      <p class="desc">天从云之剑</p>
      <div class="play">开玩</div>
    </div>
    <div class="list-ii">
      <div class="item" v-for="item of listII" :key="item.id">
        <img class="icon" :src="item.url">
        <p class="item-desc">{{ item.desc }}</p>
      </div>
    </div>
  </div>
</template>

<script type="text/ecmascript-6">
export default {
  name: 'NewGame',
  data () {
    return {
      listII: [{
        id: '001',
        url: 'https://open.shandw.com/uploads/446767319f7ef0d23ef398b191bcb908.png',
        desc: '斗地主'
      }, {
        id: '002',
        url: 'https://open.shandw.com/uploads/8fc46a91a9ee470695c014a5261e6db4.png',
        desc: '仙魔神域'
      }, {
        id: '003',
        url: 'https://open.shandw.com/uploads/b989ade28eb919e2a8d163ea11b6bd2b.png',
        desc: '萌鸡快跑'
      }, {
        id: '004',
        url: 'https://open.shandw.com/uploads/881aaed54b537df3b09c73d7843f1ec0.png',
        desc: '寻龙剑'
      }, {
        id: '005',
        url: 'https://open.shandw.com/uploads/424c015778c6e2ba644a81ed63b0defd.png',
        desc: '就决定是你了'
      }
      ]
    }
  }
}
</script>

<style lang="stylus" rel="stylesheet/stylus" scoped>
  @import "~@/assets/styles/varibles.styl"
  .wrapper
    background: $bgColor
    margin-top: .24rem
    padding: .3rem
    position: relative
    .title
      position relative
      text-align: center
      width: 1.12rem
      margin: 0 auto
      &:before
        content:""
        width: .2rem
        height: .04rem
        position absolute
        top: 50%
        border-radius: .02rem
        background: #23c9b6
        left: -.24rem
      &:after
        content:""
        width: .2rem
        height: .04rem
        position absolute
        top: 50%
        border-radius: .02rem
        background: #23c9b6
        right: -.24rem
    .arrow
      display: inline-block
      width: .32rem
      height: .32rem
      background: url('../../../assets/imgs/rightarrow.png') no-repeat
      background-size: 100%
      position: absolute
      right: .3rem
      top: .3rem
    .list-ii
      height: 1.6rem
      display: flex
      min-width: 0
      padding: .2rem 0 0 0
      justify-content: space-between
      .item
        height: 1.6rem
        width: 1.15rem
        position: relative
        .icon
          display: block
          width: 1.14rem
          height: 1.14rem
          border-radius: .26rem
        .item-desc
          width: 1.15rem
          height: .48rem
          line-height: .48rem
          position: absolute
          bottom: 0rem
          text-align: center
          ellipsis()
    .banner
      padding: .2rem 0 0 0
      position: relative
      .img-wrap
        overflow: hidden
        height: 0
        padding-bottom: 33.8%
        position: relative
        .img
          width: 100%
          display: block
          border-radius: .16rem
        .tag
          width: .46rem
          height: .53rem
          position: absolute
          top: 0rem
          right: 0.1rem
          background: url('../../../assets/imgs/dujia.png') no-repeat
          background-size: 100%
      .desc
        height: .52rem
        line-height: .52rem
        font-size: .32rem
        position: absolute
        bottom: 0.2rem
        left: 0.56rem
      .play
        width: 1.14rem
        height: .52rem
        border-radius: .251rem
        line-height: .5rem
        background: linear-gradient(90deg,#22cab5,#3fe28f)
        font-size: .32rem
        color: #ffffff
        text-align center
        position: absolute
        font-size: .32rem
        right: 0.4rem
        bottom: 0.2rem
</style>
