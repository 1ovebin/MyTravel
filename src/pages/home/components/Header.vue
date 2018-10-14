<template>
  <div class="home-header">
    <div class="header-left">
      <div class="iconfont back-icon">&#xe624;</div>
    </div>
    <div class="header-input">
      <span class="iconfont search-icon">&#xe632;</span>
      输入城市/景点/游玩主题
    </div>
    <router-link class="header-right" tag="div" to="/city">
      {{this.city}}
      <span class="iconfont city-icon">&#xe6aa;</span>
    </router-link>
  </div>
</template>

<script>
export default {
  name: 'HomeHeader',
  props: {
    city: String
  }
}
</script>

<style scoped>
  .home-header{display: flex;height: .86rem;line-height: .86rem;background: #00bcd4;color: #fff}
  .header-left{float: left;width: .8rem}
  .back-icon{font-size: .35rem;text-align: center;font-weight: bold}
  .header-input{flex: 1;height: .6rem;line-height: .6rem;background: #fff;border-radius: .08rem;margin-left: .2rem;margin: .14rem auto;color: #ccc;padding-left: .2rem}
  .search-icon,.city-icon{vertical-align: bottom}
  .header-right{float: right;width: 1.28rem;margin-left: -.04rem;text-align: center}
  .link-color{color: #fff;}
</style>
