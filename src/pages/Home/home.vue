<template>
  <div>
    <HomeHeader></HomeHeader>
    <HomeSwiper></HomeSwiper>
    <HomeIcon></HomeIcon>
    <HomeRecommend></HomeRecommend>
    <HomeRecommendSwiper></HomeRecommendSwiper>
    <SmallGame></SmallGame>
    <NewGame></NewGame>
    <NewServer></NewServer>
    <HomeNotice></HomeNotice>
    <AllGame></AllGame>
  </div>
</template>

<script type="text/ecmascript-6">
import HomeHeader from './components/HomeHeader.vue'
import HomeSwiper from './components/HomeSwiper.vue'
import HomeIcon from './components/HomeIcon.vue'
import HomeRecommend from './components/HomeRecommend.vue'
import HomeRecommendSwiper from './components/HomeRecommendSwiper.vue'
import SmallGame from './components/SmallGame.vue'
import NewGame from './components/NewGame.vue'
import NewServer from './components/NewServer.vue'
import HomeNotice from './components/HomeNotice.vue'
import AllGame from './components/AllGame.vue'
export default {
  components: {
    HomeHeader,
    HomeSwiper,
    HomeIcon,
    HomeRecommend,
    HomeRecommendSwiper,
    SmallGame,
    NewGame,
    NewServer,
    HomeNotice,
    AllGame
  }
}
</script>

<style lang="stylus" rel="stylesheet/stylus" scoped>

</style>
