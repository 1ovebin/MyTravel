<template>
  <div class="ct-header-container">
    <div class="ct-header">
      <router-link to="/">
        <div class="ct-header-left iconfont">&#xe624;</div>
      </router-link>
      <h1 class="ct-header-title">城市选择</h1>
    </div>
    <div class="ctHeader-tabs">
      <ul class="ct-tab-list">
        <li class="ct-tab-li" v-for="(item,index) in tabs" :key="index" :class="{active:index == nowIndex}" @click="tab(index)">{{item}}</li>
      </ul>
    </div>
    <city-churchyard v-show="nowIndex===0"></city-churchyard>
    <city-overseas v-show="nowIndex===1"></city-overseas>
  </div>
</template>

<script>
import cityChurchyard from '@/pages/city/components/Churchyard'
import cityOverseas from '@/pages/city/components/Overseas'
export default {
  name: 'CityHeader',
  components: {
    cityChurchyard,
    cityOverseas
  },
  data () {
    return {
      tabs: ['境内', '境外·港澳台'],
      nowIndex: 0,
      isShow: false
    }
  },
  methods: {
    tab (index) {
      this.nowIndex = index
    }
  }
}
</script>

<style scoped>
  .ct-header{height: .68rem;line-height: .68rem;border-bottom: 0;position: relative;background: #00bcd4;z-index: 90}
  .ct-header-left{position: absolute;left: 0;top: 0;width: .8rem;height: .88rem;line-height: .88rem;font-size: .36rem;color: #fff;text-align: center;font-weight: bold}
  .ct-header-title{overflow: hidden;margin: 0 1rem;line-height: .88rem;white-space: nowrap;text-overflow: ellipsis;font-size: .32rem;text-align: center;color: #fff}
  /*  */
  .ctHeader-tabs{height: .4rem;line-height: .4rem;background-color: #00bcd4;padding: .2rem 1rem;color: #fff}
  .ct-tab-list{overflow: hidden;border: 1px solid #fff;border-radius: .03rem;zoom: 1}
  .ct-tab-li{width: 50%;float: left;text-align: center;background-color: #00bcd4;font-size: .28rem;color: #fff}
  .active{background-color: #fff;color: #00bcd4;}
</style>
