<template>
  <div class="slider" ref="slider">
    <div class="slider-group border-top" ref="sliderGroup">
      <div class="item" v-for="item of list" :key="item.id">
        <div class="img-wrap">
          <img class="item-img" :src="item.url">
        </div>
        <div class="item-white"></div>
        <p class="item-title">{{ item.title}}</p>
        <p class="item-desc">{{ item.desc }}</p>
        <div class="spec">
          <img class="tags" v-if="item.tags[0]" src="../../../assets/imgs/dujia.png">
          <img class="tags" v-if="item.tags[1]" src="../../../assets/imgs/jingpin.png">
          <img class="tags" v-if="item.tags[2]" src="../../../assets/imgs/shoufa.png">
          <img class="tags" v-if="item.tags[3]" src="../../../assets/imgs/gift.png">
        </div>
      </div>
   </div>
  </div>
</template>

<script type="text/ecmascript-6">
import BScroll from 'better-scroll'
export default {
  name: 'HomeRecommendSwiper',
  mounted () {
    this.InitTabScroll()
  },
  methods: {
    InitTabScroll () {
      let width = 0
      for (let i = 0; i < this.list.length; i++) {
        width += this.$refs.sliderGroup.children[i].getBoundingClientRect().width
      }

      this.$refs.sliderGroup.style.width = width / 50 + (this.list.length * 0.4) + 'rem'
      this.$nextTick(() => {
        if (!this.scroll) {
          this.scroll = new BScroll(this.$refs.slider, {
            startX: 0,
            click: true,
            scrollX: true,
            scrollY: false,
            eventPassthrough: 'vertical'
          })
        }
      })
    }
  },
  data () {
    return {
      list: [
        {
          id: '001',
          url: 'https://open.shandw.com/uploads/f7c1737bd5feaa94ff4664b676ee1575.png  ',
          title: '天丛云之剑',
          desc: '二次元小姐姐带回家',
          tags: ['01', false, false, false]
        },
        {
          id: '002',
          url: 'https://open.shandw.com/uploads/640b40cba22582d25e4cc531dd85234c.png',
          title: '斗地主',
          desc: '赢闪电币 换大米啦',
          tags: [false, '02', false, false]
        },
        {
          id: '003',
          url: 'https://www.shandw.com/h5/h5gameimg/hjxl03.png',
          title: '小黄鸡下楼',
          desc: '火爆的魔性小游戏',
          tags: [false, false, false, false]
        },
        {
          id: '004',
          url: 'https://open.shandw.com/uploads/5d41fff686b5f29cb3617cb8ff48c1db.png',
          title: '斗罗大陆H5',
          desc: '正版IP授权挂机类网游',
          tags: [false, false, '03', '04']
        },
        {
          id: '005',
          url: 'https://open.shandw.com/uploads/ed5c54da9f12164f9bb1b48d16350cc7.png',
          title: '我要修仙',
          desc: '纯正修仙，跨服抢怪！',
          tags: [false, false, '03', false]
        },
        {
          id: '006',
          url: 'https://www.shandw.com/h5/h5gameimg/BJZH03.jpg',
          title: '百将斩',
          desc: '爽快三国，指尖纵横',
          tags: ['01', false, false, false]
        },
        {
          id: '007',
          url: 'https://open.shandw.com/uploads/f7c1737bd5feaa94ff4664b676ee1575.png  ',
          title: '天丛云之剑',
          desc: '二次元小姐姐带回家',
          tags: ['01', false, false, false]
        },
        {
          id: '008',
          url: 'https://open.shandw.com/uploads/f7c1737bd5feaa94ff4664b676ee1575.png  ',
          title: '天丛云之剑',
          desc: '二次元小姐姐带回家',
          tags: ['01', false, false, false]
        },
        {
          id: '009',
          url: 'https://open.shandw.com/uploads/f7c1737bd5feaa94ff4664b676ee1575.png  ',
          title: '天丛云之剑',
          desc: '二次元小姐姐带回家',
          tags: ['01', false, false, false]
        },
        {
          id: '010',
          url: 'https://open.shandw.com/uploads/f7c1737bd5feaa94ff4664b676ee1575.png  ',
          title: '天丛云之剑',
          desc: '二次元小姐姐带回家',
          tags: ['01', false, false, false]
        }
      ]
    }
  }
}
</script>

<style lang="stylus" rel="stylesheet/stylus" scoped>
  @import "~@/assets/styles/varibles.styl"
  .slider-group
    height: 3.19rem
    padding: .32rem 0rem .32rem .3rem
    background: $bgColor
    color: #000
    overflow:hidden
    .item
      display: inline-table
      width: 2.87rem
      height: 3.09rem
      border-radius: .16rem
      position relative
      float: left
      margin-right: .4rem
      .img-wrap
        position: absolute
        top: 0
        left: 0
        height: 2rem
        width: 100%
        .item-img
          display block
          border-top-right-radius: .16rem
          border-top-left-radius: .16rem
          width: 100%
      .item-white
        width: 100%
        height: 1.1rem
        background: #ffffff
        position:absolute
        border-bottom-right-radius: .16rem
        border-bottom-left-radius: .16rem
        bottom: 0
      .item-title
        height: .44rem
        width: 100%
        top: 2.1rem
        position: absolute
        text-align: center
        font-size: .32rem
      .item-desc
        color: #666666
        height: .44rem
        font-size: .26rem
        width: 100%
        top: 2.6rem
        position: absolute
        text-align: center
      .spec
        position:absolute
        right: 0
        top: 0
        .tags
          width: .5rem
          height: .6rem
          float: right
          margin: .032rem
</style>
