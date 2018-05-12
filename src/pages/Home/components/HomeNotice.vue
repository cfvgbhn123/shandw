<template>
  <div class="wrapper">
    <div class="title">
      闪电资讯
    </div>
    <span class="arrow"></span>
    <div class="container">
      <div class="item" v-for="item of list" :key="item.id">
        <span class="tag blue" v-if="item.flag">{{ item.tag }}</span>
        <span class="tag orange" v-else >{{ item.tag }}</span>
        <p class="item-title">{{ item.title }}</p>
        <div class="date">{{ item.date }}</div>
      </div>
    </div>
  </div>
</template>

<script type="text/ecmascript-6">
export default {
  name: 'HomeNotice',
  data () {
    return {
      list: [
        {
          id: '001',
          tag: '活动',
          title: '《蜀山世界》-踏火歌行母亲节活动《蜀山世界》-踏火歌行母亲节活动',
          date: '5-11',
          flag: false
        }, {
          id: '002',
          tag: '活动',
          title: '《红月无双》5.12-5.16活动',
          date: '5-11',
          flag: false
        }, {
          id: '003',
          tag: '公告',
          title: '《百战沙城》合服公告',
          date: '5-11',
          flag: true
        }, {
          id: '004',
          tag: '活动',
          title: '【决战沙城】5.12感恩母亲节活动',
          date: '5-11',
          flag: false
        }, {
          id: '005',
          tag: '活动',
          title: '【荣耀足球】-母亲节活动',
          date: '5-11',
          flag: false
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
    padding-top: .3rem
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
        transform: translateY(-50%)
        border-radius: .02rem
        background: #23c9b6
        left: -.24rem
      &:after
        content:""
        width: .2rem
        height: .04rem
        position absolute
        top: 50%
        transform: translateY(-50%)
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
    .container
      padding: .2rem .3rem 0 .3rem
      position: relative
      .item
        height: .89rem
        position: relative
        .tag
          width: .48rem
          height: .32rem
          line-height: .32rem
          font-size: .24rem
          padding: .04rem
          border-radius: .12rem
          position: absolute
          top: 50%
          left: 0 rem
          transform: translateY(-50%)
        .orange
          border: 2px solid #fe8731;
          color: #fe8731
        .blue
          border: 2px solid #24b9a9
          color: #24b9a9
        .item-title
          height: .8rem
          position: absolute
          top: 50%
          transform: translateY(-50%)
          line-height: .8rem
          left: .8rem
          ellipsis()
          max-width: 70%
        .date
          height: .8rem
          position: absolute
          top: 50%
          transform: translateY(-50%)
          line-height: .8rem
          right: 0 rem
          color: #6c7583
</style>
