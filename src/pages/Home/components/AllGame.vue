<template>
  <div class="wrapper">
    <div class="title">
      全部游戏
    </div>
    <div class="container border-bottom">
      <div class="item" v-for="item of list" :key="item.id">
        <img :src="item.url" class="game-icon">
        <div class="item-title">
          <div class="game-name">
            {{ item.name }}
            <span class="tag jingpin" v-show="item.tags[0]">精品</span>
            <span class="tag libao" v-show="item.tags[1]">礼包</span>
            <span class="tag remen" v-show="item.tags[2]">热门</span>
            <span class="tag shoufa" v-show="item.tags[3]">首发</span>
            <span class="tag zuixin" v-show="item.tags[4]">最新</span>
          </div>
          <div class="game-desc">{{ item.desc }}<span class="number-wrap"><i class="number border-left">{{ item.number }}</i></span>人在玩</div>
          <div class="slogen">{{ item.slogen }}</div>
        </div>
        <span class="play">开玩</span>
      </div>
    </div>
  </div>
</template>

<script type="text/ecmascript-6">
export default {
  name: 'AllGame',
  data () {
    return {
      list: [
        {
          id: '001',
          url: 'https://www.shandw.com/h5/h5gameimg/JZ04.png',
          name: '决战沙城',
          desc: '传奇类',
          number: '184.2万',
          slogen: '十年兄弟，再战沙城！',
          tags: [1, 1, 0, 0, 0]
        }, {
          id: '002',
          url: 'https://www.shandw.com/h5/h5gameimg/MDHW04-2.gif',
          name: '梦道',
          desc: '回合制',
          number: '83.6万',
          slogen: '浪漫回合，尽在梦道！',
          tags: [0, 1, 1, 0, 0]
        }, {
          id: '003',
          url: 'https://open.shandw.com/uploads/f0345d120db2a2de51e5a94d2c3c281e.png',
          name: '侠客行',
          desc: '古装仙侠',
          number: '65.5万',
          slogen: '独步天下，踏雪无痕',
          tags: [1, 1, 0, 0, 0]
        }, {
          id: '004',
          url: 'https://www.shandw.com/h5/h5gameimg/MXYT04.png',
          name: '冒险与推图',
          desc: '策略',
          number: '168.1万',
          slogen: '只有5%的人能通关',
          tags: [0, 0, 1, 0, 0]
        }, {
          id: '005',
          url: 'https://open.shandw.com/uploads/a901784914f64584d41fd68346affaae.png',
          name: '店长也疯狂',
          desc: '策略',
          number: '63.2万',
          slogen: '小姐姐叫你来开店',
          tags: [1, 1, 0, 0, 0]
        }, {
          id: '006',
          url: 'https://www.shandw.com/h5/h5gameimg/WCBYHW04.png',
          name: '三国霸业',
          desc: '传奇类',
          number: '64.3万',
          slogen: '三国时代，一起战斗!',
          tags: [0, 1, 1, 0, 0]
        }, {
          id: '007',
          url: 'https://open.shandw.com/uploads/b937242977a2e763c8eaea7a8bdaa97d.png',
          name: '怼怼三国',
          desc: '策略',
          number: '59.4万',
          slogen: '90秒——轻策略——卡牌对',
          tags: [0, 0, 0, 1, 0]
        }, {
          id: '008',
          url: 'https://open.shandw.com/uploads/3d594030912346ebe11c80810daf036b.png',
          name: '骑战三国',
          desc: '卡牌',
          number: '57.7万',
          slogen: '三国群英，尽收麾下！',
          tags: [0, 1, 0, 0, 1]
        }, {
          id: '009',
          url: 'https://open.shandw.com/uploads/0d0039f39480ff4ee77bc1322e4774f6.png',
          name: '修罗武神',
          desc: '放置挂机',
          number: '27.7万',
          slogen: '正版授权H5游戏新贵',
          tags: [0, 1, 0, 1, 0]
        }, {
          id: '010',
          url: 'https://open.shandw.com/uploads/ed37129918df7983d6a013e659a601dd.png',
          name: '野蛮人大作战H5',
          desc: '休闲小游戏',
          number: '9.6万',
          slogen: '自由自在野蛮像素战',
          tags: [1, 0, 0, 0, 0]
        }
      ]
    }
  }
}
</script>

<style lang="stylus" rel="stylesheet/stylus" scoped>
  @import "~@/assets/styles/varibles.styl"
  .wrapper
    padding: .3rem .3rem .3rem .3rem
    margin-top .24rem
    background: $bgColor
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
    .container
      padding: .18rem 0 .18rem 0
      position: relative
      .item
        position: relative
        height: 1.2rem
        width: 100%
        margin: .3rem 0 .2rem 0
        .game-icon
          display: block
          position: absolute
          top: 0
          left: 0
          width: 1.2rem
          height: 1.2rem
          border-radius: .18rem
        .item-title
          width: 4.1rem
          position: absolute
          top: 0rem
          left: 1.3rem
          height: 1.2rem
          .game-name
            float: left
            width: 6rem
            line-height: .4rem
            margin: 0rem
            font-size: .28rem
            .tag
              width: .48rem
              height: .3rem
              line-height: .3rem
              box-sizing:border-box
              padding: .02rem
              border-radius: .1rem
            .jingpin
              background: #8b65f5
            .libao
              background: #e7af42
            .remen
              background: #e45263
            .shoufa
              background: #3589d7
            .zuixin
              background:#df6b39
          .game-desc
            line-height: .4rem
            color: #6c7583
            .number-wrap
              .number
                color: #d77d12
                font-weight: 700
                font-style: italic
                padding: 0 .1rem 0 .1rem
                margin-left: .1rem
          .slogen
            width: 5.1rem
            position: absolute
            bottom: 0
            left: 0
            color: #6c7583
        .play
          width: 1.14rem
          height: .52rem
          border-radius: .251rem
          line-height: .5rem
          background: linear-gradient(90deg,#22cab5,#3fe28f)
          font-size: .28rem
          color: #ffffff
          text-align center
          position: absolute
          right: 0.1rem
          top: 50%;
          transform: translateY(-50%)
</style>
