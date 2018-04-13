<template>
  <div>
      <home-header></home-header>
      <div class="home-content" ref="wrapper">
         <div>
            <home-swiper :list="swiperList"></home-swiper>
            <home-icons :list="iconList"></home-icons>
            <home-recommend :list="recommendList"></home-recommend>
            <home-weekend :list="weekendList"></home-weekend>
         </div>
      </div>
     
  </div>
</template>

<script>
import HomeHeader from './components/Header'
import HomeSwiper from './components/Swiper'
import HomeIcons from './components/Icons'
import HomeRecommend from './components/Recommend'
import HomeWeekend from './components/Weekend'
import axios from 'axios'
import Bscroll from 'better-scroll'

export default {
  name: 'Home',
  data () {
    return {
      swiperList:[],
      iconList:[],
      recommendList:[],
      weekendList:[]
    }
  },
  components: {
    HomeHeader,
    HomeSwiper,
    HomeIcons,
    HomeRecommend,
    HomeWeekend
  },
  methods:{
    getHomeInfo () {
       axios.get('/api/index.json')
         .then(this.getHomeInfoSucc)
    },
    getHomeInfoSucc (res) {
      res = res.data
      if(res.ret && res.data){
        const data = res.data
        this.swiperList = data.swiperList
        this.iconList = data.iconList
        this.recommendList = data.recommendList
        this.weekendList = data.weekendList
      }
      console.log(res)
    }
  },
  mounted () {
    this.scroll = new Bscroll(this.$refs.wrapper)
    this.getHomeInfo()
  }
}
</script>

<style lang="scss" scoped>
@import "~styles/varibles.scss";
.home-content{
  position: absolute;
  overflow: hidden;
  top: $headerHeight;
  left: 0;
  right: 0;
  bottom: 0;
}
</style>

