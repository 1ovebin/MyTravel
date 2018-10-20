<template>
  <div>
    <div class="banner-back" v-show="showAbs" @click="backClick">
      <span class="iconfont back-icon">&#xe600;</span>
    </div>
    <div class="header-fixed" v-show="!showAbs" :style="opacityStyle">
      <router-link to="/">
        <div class="iconfont header-fixed-back">&#xe624;</div>
      </router-link>
      景点详情
    </div>
  </div>
</template>

<script>
export default {
  name: 'DetailHeader',
  data () {
    return {
      showAbs: true,
      opacityStyle: {
        opacity: 0
      }
    }
  },
  methods: {
    backClick () {
      this.$router.go(-1)
    },
    handleScroll () {
      const top = document.documentElement.scrollTop
      if (top > 60) {
        let opacity = top / 140
        opacity = opacity > 1 ? 1 : opacity
        this.opacityStyle = { opacity }
        this.showAbs = false
      } else {
        this.showAbs = true
      }
    }
  },
  mounted () {
    window.addEventListener('scroll', this.handleScroll)
  },
  unmounted () {
    window.removeEventListener('scroll', this.handleScroll)
  }
}
</script>

<style scoped>
  /* banner-back */
  .banner-back{position: absolute;left: .15rem;top: .15rem;width: .72rem;height: .72rem;line-height: .72rem;opacity: .5;}
  .back-icon{font-size: .8rem;}
  .header-fixed{z-index: 2;position: fixed;top: 0;left: 0;right: 0;height: .88rem;line-height: .88rem;text-align: center;color: #fff;background: #00BCD4; font-size: .32rem;}
  .header-fixed-back{position: absolute;top: 0;left: 0;width: .64rem;text-align: center;font-size: .4rem;color: #fff}
</style>
