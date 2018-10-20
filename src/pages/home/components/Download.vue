<template>
  <div class="foot-download" v-show="downloadShow">
    <span class="download-close" @click="downloadClick">X</span>
    <span class="download-logo"></span>
    <p class="download-des">使用去哪儿门票客户端<br>享受专属优惠体验更流畅</p>
    <a class="download-btn" href="javascript:void(0)">立即下载</a>
  </div>
</template>

<script>
export default {
  name: 'HomeFoot',
  data () {
    return {
      downloadShow: true
    }
  },
  methods: {
    downloadClick () {
      this.downloadShow = false
    }
  }
}
</script>

<style scoped>
  .foot-download{position: fixed;z-index: 20;bottom: 0;left: 0;height: 1rem;background: rgba(0,0,0,.8);width: 100%;}
  .download-close{display: inline-block;position: absolute;top: 0;left: 0;width: .5rem;height: .5rem;line-height: .4rem;text-indent: .1rem;background: #afafaf;-webkit-border-radius: 0 0 .5rem 0;-moz-border-radius: 0 0 .5rem 0;-o-border-radius: 0 0 .5rem 0;-ms-border-radius: 0 0 .5rem 0;border-radius: 0 0 .5rem 0;color: #fff;}
  .download-logo{display: inline-block;position: relative;top: .15rem;left: .65rem;width: .7rem;height: .7rem;background: url(http://imgs.qunarzz.com/piao/fusion/1606/44/2605d5bd522e109a.png);background-size: .7rem .7rem;-webkit-border-radius: .1rem;-moz-border-radius: .1rem;-o-border-radius: .1rem;-ms-border-radius: .1rem;border-radius: .1rem;}
  .download-des{position: absolute;left: 1.6rem;top: .2rem;line-height: .32rem;font-size: .24rem;color: #fff;}
  .download-btn{position: absolute;display: block;top: .22rem;right: .2rem;width: 1.4rem;height: .56rem;line-height: .56rem;text-align: center;border: .02rem solid #1d8f96;-webkit-border-radius: .08rem;-moz-border-radius: .08rem;-o-border-radius: .08rem;-ms-border-radius: .08rem;border-radius: .08rem;font-size: .26rem;color: #1d8f96;}
</style>
