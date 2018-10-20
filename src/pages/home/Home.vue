<template>
  <div class="page-container">
    <home-header :city="city"></home-header>
    <home-swiper :swiperList="swiperList"></home-swiper>
    <home-icons :iconsList="iconsList"></home-icons>
    <home-special :specList="specList"></home-special>
    <home-hot-sale :hotList="hotList"></home-hot-sale>
    <home-recommend :recoList="recoList"></home-recommend>
    <home-weekend :weekendList="weekendList"></home-weekend>
    <home-download></home-download>
    <home-footer></home-footer>
  </div>
</template>

<script>
import HomeHeader from '@/pages/home/components/Header'
import HomeSwiper from '@/pages/home/components/Swiper'
import HomeIcons from '@/pages/home/components/Icons'
import HomeSpecial from '@/pages/home/components/Special'
import HomeHotSale from '@/pages/home/components/HotSale'
import HomeRecommend from '@/pages/home/components/Recommend'
import HomeWeekend from '@/pages/home/components/Weekend'
import HomeDownload from '@/pages/home/components/Download'
import HomeFooter from '@/pages/home/components/Footer'
import axios from 'axios'
export default {
  name: 'Home',
  components: {
    HomeHeader,
    HomeSwiper,
    HomeIcons,
    HomeSpecial,
    HomeHotSale,
    HomeRecommend,
    HomeWeekend,
    HomeDownload,
    HomeFooter
  },
  data () {
    return {
      city: '',
      swiperList: [],
      iconsList: [],
      specList: [],
      hotList: [],
      recoList: [],
      weekendList: []
    }
  },
  methods: {
    getHomeInfo () {
      axios.get('/api/index.json')
        .then(this.getHomeInfoSucc)
    },
    getHomeInfoSucc (res) {
      if (res.data.ret && res.data) {
        const data = res.data.data
        this.city = data.city
        this.swiperList = data.swiperList
        this.iconsList = data.iconsList
        this.specList = data.specList
        this.hotList = data.hotList
        this.recoList = data.recoList
        this.weekendList = data.weekendList
      }
    }
  },
  mounted () {
    this.getHomeInfo()
  }
}
</script>

<style scoped>
  .page-container{width: 100%;height: 100%;background: #f5f5f5}
</style>
