<template>
  <div class="wrapper">
    <div class="title border-bottom">

      <input type="radio" id="old" name="new-server" checked  @click="change">
      <label for="old" class="nav1">已新开服</label>
      <input type="radio" id="new" name="new-server" @click="change">
      <label for="new" class="nav2">新服预告</label>
    </div>

    <div class="container border-bottom" v-show="flag">
      <div class="item" v-for="item of list" :key="item.id">
        <img :src="item.url" class="game-icon">
        <div class="item-title">
          <div class="game-name">{{ item.name }}</div>
          <div class="game-server">{{ item.server }}</div>
        </div>
        <div class="server-time">{{ item.time }}</div>
        <span class="play">开玩</span>
      </div>
    </div>

    <div class="container border-bottom" v-show="!flag">
      <div class="item" v-for="item of listI" :key="item.id">
        <img :src="item.url" class="game-icon">
        <div class="item-title">
          <div class="game-name">{{ item.name }}</div>
          <div class="game-server">{{ item.server }}</div>
        </div>
        <div class="server-time">{{ item.time }}</div>
        <span class="play">开玩</span>
      </div>
    </div>
    <div class="more">
      <span class="text">查看更多</span>
    </div>
  </div>
</template>

<script type="text/ecmascript-6">
export default {
  name: 'NewServer',
  data () {
    return {
      flag: true,
      list: [
        {
          id: '001',
          url: 'https://open.shandw.com/uploads/abfa7f8d327bffa7697c2c536c5801b1.png',
          name: '萌斗魏蜀吴',
          server: '百骑袭营',
          time: '新开服'
        }, {
          id: '002',
          url: 'https://open.shandw.com/uploads/68bb548b08381f7c28a9fd14bafc2e66.png',
          name: '决战荣耀（决战魔域）',
          server: '魔域312服',
          time: '新开服'
        }, {
          id: '003',
          url: 'https://open.shandw.com/uploads/7b5e8350b6d702adc6ab1dd4f8873742.png',
          name: '楚乔传之谍纸天眼',
          server: '官方96服',
          time: '新开服'
        }, {
          id: '004',
          url: 'https://www.shandw.com/h5/h5gameimg/LCBY04.png',
          name: '龙城霸业',
          server: '689服',
          time: '新开服'
        }, {
          id: '005',
          url: 'https://www.shandw.com/h5/h5gameimg/BZSC04.jpg',
          name: '百战沙城',
          server: '百战359区',
          time: '新开服'
        }
      ],
      listI: [
        {
          id: '001',
          url: 'https://open.shandw.com/uploads/3d594030912346ebe11c80810daf036b.png',
          name: '骑战三国',
          server: '智取仁守',
          time: '今日14:00'
        }, {
          id: '002',
          url: 'https://open.shandw.com/uploads/f0345d120db2a2de51e5a94d2c3c281e.png',
          name: '侠客行',
          server: '巧春',
          time: '今日15:00'
        }, {
          id: '003',
          url: 'https://open.shandw.com/uploads/b07649f775b775123e8d525ae4e433c9.png',
          name: '开心国王',
          server: '雾里看花',
          time: '今日18:00'
        }, {
          id: '004',
          url: 'https://www.shandw.com/h5/h5gameimg/LCBY04.png',
          name: '七十二变',
          server: '长安200服',
          time: '今日17:00'
        }, {
          id: '005',
          url: 'https://www.shandw.com/h5/h5gameimg/DTSZJ004-1.gif',
          name: '大天使之剑H5',
          server: '公测423服',
          time: '今日17:00'
        }
      ]
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
  .wrapper
    margin-top: .24rem
    padding: .3rem
    background: $bgColor
    .title
      height: .8rem
      display: relative
      input[type=radio]
        display: none
      .nav1
        display: inline-block
        width: 30%
        text-align: center
        color: #6c7583
        height: .8rem
        line-height: .8rem
        font-size: .32rem
        position: absolute
        left: 50%
        transform: translateX(-100% )
      .nav2
        display: inline-block
        width: 30%
        text-align: center
        color: #6c7583
        height: .8rem
        line-height: .8rem
        font-size: .32rem
        position: absolute
        right: 50%
        transform: translate(100%)
      :checked + label
        color: #ffffff
        &:after
          content: "";
          width: 1.3rem;
          height: .04rem;
          border-radius: .02rem;
          background: #23c9b6;
          position: absolute;
          bottom: 0;
          left: 50%;
          transform: translate(-50%)
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
          width: 2.6rem
          position: absolute
          top: 0rem
          left: 1.3rem
          .game-name
            line-height: .4rem
            margin: .3rem 0 .06rem 0
            font-size: .34rem
            ellipsis()
          .game-server
            line-height: .4rem
            color: #fe8731
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
          right: 0.1rem
          top: 50%;
          transform: translateY(-50%)
        .server-time
          position: absolute;
          top: 50%;
          color:#6c7583
          transform: translateY(-50%)
          right: 1.4rem
          font-size: .32rem
    .more
      height: 1rem
      width: 1.2rem
      margin: 0 auto
      line-height: .5rem
      text-align: center
      color: #6c7583
      font-size: .3rem
      position: relative
      .text
        position: absolute
        top: 50%
        left: 50%
        width: 1.2rem
        transform: translate(-50%,-50%)
        &:after
          content: ""
          display: block
          width: .2rem
          height: .24rem
          position: absolute
          background: url('../../../assets/imgs/more.png')  50% 50% no-repeat
          background-size: .2rem .4rem
          top: 50%
          transform: translate(150%,-50%)
          right: 0rem
</style>
