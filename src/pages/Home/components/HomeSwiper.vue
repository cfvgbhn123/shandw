<template>
  <div>
    <swiper :options="swiperOption" class="swiper-wrap">
      <swiper-slide class="slider">
        <img class="swiper-img" src="https://open.shandw.com/uploads/0fb9f7dc2ee122f018e619b74e210148.png">
      </swiper-slide>
      <swiper-slide class="slider">
        <img class="swiper-img" src="https://open.shandw.com/uploads/e096eb5a388c56d23bd3d157a62db95a.png">
      </swiper-slide>
      <swiper-slide class="slider">
        <img class="swiper-img" src="https://open.shandw.com/uploads/4aa88015f1b6b108225aabf18ce4f692.png">
      </swiper-slide>
      <div class="swiper-pagination"  slot="pagination"></div>
    </swiper>
  </div>
</template>

<script type="text/ecmascript-6">
export default {
  name: 'HomeSwiper',
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true,
        autoplay: 3000
      }
    }
  }
}
</script>

<style lang="stylus" rel="stylesheet/stylus" scoped>
  .swiper-wrap >>> .swiper-pagination-bullet-active
    background: #ffffff
    width: .1rem
    height: .1rem
    margin-bottom: 0 .1rem -.1rem .1rem
  .swiper-wrap
    .slider
      margin: 0 auto
      height: 0
      overflow: hidden
      padding-bottom: 34.03%
      .swiper-img
        width: 100%
</style>
