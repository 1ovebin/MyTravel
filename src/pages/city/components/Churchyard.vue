<template>
  <div class="city-list-container" ref="wrapper">
    <div>
      <h2 class="city-hot">热门城市</h2>
      <ul class="hot-list hot-tr3">
        <li class="ct-list-dec ct-hot" v-for="item of hotCities" :key="item.id">{{item.name}}</li>
      </ul>
      <h2 class="city-hot">字母排序</h2>
      <ul class="ct-character-list ct-tr6">
        <li class="ct-letter" v-for="(item, key) of cities" :key="key" @click="letterClick" @change="letterChange">{{key}}</li>
      </ul>
      <div class="city-letter" v-for="(item, key) of cities" :key="key" :ref="key">
        <h2 class="city-hot">{{key}}</h2>
        <ul class="hot-list">
          <li class="ct-list-dec" v-for="innerItem of item" :key="innerItem.id">{{innerItem.name}}</li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
import axios from 'axios'
import BScroll from 'better-scroll'
export default {
  name: 'CityChurchyard',
  data () {
    return {
      hotCities: [],
      cities: [],
      letter: ''
    }
  },
  methods: {
    getCityInfo () {
      axios.get('/api/city.json')
        .then(this.getCityInfoSucc)
    },
    getCityInfoSucc (res) {
      if (res.data.ret && res.data) {
        const data = res.data.data
        this.hotCities = data.hotCities
        this.cities = data.cities
      }
    },
    letterClick (e) {
      this.letter = e.target.innerText
    },
    letterChange (letter) {
      console.log(letter)
    }
  },
  mounted () {
    this.getCityInfo()
    this.scroll = new BScroll(this.$refs.wrapper)
  },
  watch: {
    letter () {
      // console.log(this.letter)
      if (this.letter) {
        const element = this.$refs[this.letter][0]
        console.log(this.$refs[this.letter][0])
        this.scroll.scrollToElement(element)
      }
    }
  }
}
</script>

<style>
  .city-list-container{position: absolute;top: 1.48rem;left: 0;right: 0;bottom: 0;overflow: hidden;}
  .city-hot{display: block;font-size: .24rem;padding: .24rem .3rem;background: #F5F5F5;}
  .hot-list{position: relative;overflow: hidden;z-index: 0;background-color: #fff;}
  .hot-list:before{content: '';position: absolute;width: 25%;left: 25%;height: 100%;border-left: .02rem solid #ddd;border-right: .02rem solid #ddd;}
  .hot-tr3:before{width: 33.33%;left: 33.33%;}
  .hot-list:after{content: '';position: absolute;width: 10%;left: 75%;height: 100%;border-left: .02rem solid #ddd;border-right: 0;}
  .hot-tr3:after{border: 0}
  .ct-list-dec{width: 25%;height: .9rem;line-height: .9rem;font-size: .28rem;text-align: center;border-bottom: .02rem solid #ddd;margin-bottom: -1px;float: left;position: relative;z-index: 10;color: #212121;}
  .ct-hot{width: 33.33%;}
  .ct-character-list{position: relative;overflow: hidden;z-index: 0;background-color: #fff;padding: .3rem 0}
  .ct-letter{width: 16.66%;height: .9rem;line-height: .9rem;font-size: .28rem;text-align: center;float: left;position: relative;z-index: 10;color: #212121}
</style>
