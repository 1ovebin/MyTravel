<template>
  <div>
    <div class="banner">
      <img class="banner-img" src="//img1.qunarzz.com/sight/p0/1505/da/da7c46e2eef8714e.water.jpg_600x330_0170d359.jpg">
      <div class="banner-info">
        <div class="banner-num">
          <span class="iconfont banner-icon">&#xe796;</span><em class="icon-mun">12</em>
        </div>
        <div class="banner-title">千佛山(AAAA景区)</div>
      </div>
    </div>
    <!-- <gallery-list :galleryList="galleryList"></gallery-list> -->
  </div>
</template>

<script>
import GalleryList from '@/pages/detail/components/GalleryList'

export default {
  name: 'detailBanner',
  components: {
    GalleryList
  },
  data () {
    return {
      galleryList: ['http://img1.qunarzz.com/sight/p0/1505/da/da7c46e2eef8714e.water.jpg_350x240_89b0684f.jpg', 'http://img1.qunarzz.com/sight/p0/1411/c7/0c38235ff16c8547d539cdf196e09101.water.jpg_350x240_44be5894.jpg']
    }
  }
}
</script>

<style scoped>
  .banner{position: relative;overflow: hidden;width: 100%;height: 0;padding-bottom: 55%;}
  .banner-img{width: 100%;}
  .banner-num{position: absolute;left: .2rem;bottom: .86rem;width: 1.2rem;height: .4rem;background: rgba(0,0,0,.5);border-radius: .2rem;font-size: .26rem;color: #fff;line-height: .4rem;text-align: center;}
  .icon-mun{margin-left: .06rem;}
  .banner-icon{font-size: .26rem;}
  .banner-title{position: absolute;right: .2rem;bottom: .36rem;left: .2rem;min-height: .4rem;z-index: 1;line-height: .4rem;color: #fff;font-size: .36rem;text-shadow: 0 1px 2px rgba(0,0,0,0.70);}
</style>
