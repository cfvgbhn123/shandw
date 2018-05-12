<template>
  <div class="wrapper">
    <div class="title">
      小游戏
    </div>
    <span class="arrow"></span>
    <div class="list-i">
      <div class="item" v-for="item of listI" :key="item.id">
        <img class="icon" :src="item.url">
        <p class="item-desc">{{ item.desc }}</p>
      </div>
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
  name: 'SmallGame',
  data () {
    return {
      listI: [{
        id: '001',
        url: 'https://www.shandw.com/h5/h5gameimg/XFL02.jpg',
        desc: '小粉龙跳跃'
      },
      {
        id: '002',
        url: 'https://www.shandw.com/h5/h5gameimg/COLLA02.png',
        desc: '异次元穿梭'
      },
      {
        id: '003',
        url: 'https://www.shandw.com/h5/h5gameimg/BABYL02.png',
        desc: '巴比伦塔'
      },
      {
        id: '004',
        url: 'https://www.shandw.com/h5/h5gameimg/ccd04.png',
        desc: '闪电塔层层叠'
      },
      {
        id: '005',
        url: 'https://www.shandw.com/h5/h5gameimg/xsgs02.png',
        desc: '向水果发射'
      }],
      listII: [{
        id: '001',
        url: 'https://open.shandw.com/uploads/9433a28e626fbaf989ec794c4700e66c.png',
        desc: '蛇它虫'
      },
      {
        id: '002',
        url: 'https://www.shandw.com/h5/h5gameimg/BZBZ04.png',
        desc: '兵者'
      },
      {
        id: '003',
        url: 'https://open.shandw.com/uploads/dc4a0db73ec8a1ed694d3f96606bd7a4.png',
        desc: '影子来了'
      },
      {
        id: '004',
        url: 'https://open.shandw.com/uploads/90d3d3c15813a09188ed54b6bdd4df62.png',
        desc: '进化：崛起'
      },
      {
        id: '005',
        url: 'https://open.shandw.com/uploads/26e840a91783eb2426152fb5df2588b7.png',
        desc: '奔跑香肠'
      }]
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
      width: .84rem
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
    .list-i
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
</style>
