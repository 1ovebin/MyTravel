<template>
  <div>
    <div class="banner" @click="handleListShow">
      <img class="banner-img" src="//img1.qunarzz.com/sight/p0/1505/da/da7c46e2eef8714e.water.jpg_600x330_0170d359.jpg">
      <div class="banner-info">
        <div class="banner-num">
          <span class="iconfont banner-icon">&#xe796;</span><em class="icon-mun">12</em>
        </div>
        <div class="banner-title">千佛山(AAAA景区)</div>
      </div>
    </div>
    <gallery-list :galleryList="galleryList" v-show="showList"></gallery-list>
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
      showList: false,
      galleryList: ['http://img1.qunarzz.com/sight/p0/1505/da/da7c46e2eef8714e.water.jpg_350x240_89b0684f.jpg', 'http://img1.qunarzz.com/sight/p0/1411/c7/0c38235ff16c8547d539cdf196e09101.water.jpg_350x240_44be5894.jpg', 'http://img1.qunarzz.com/sight/p0/1411/ba/85805f786ced6ecd5e6376e37f71ecdd.water.jpg_350x240_0073e251.jpg', 'http://img1.qunarzz.com/sight/p0/201405/22/eb5e3869e646c287127f07271b615014.jpg_350x240_7046161e.jpg', 'http://img1.qunarzz.com/sight/p0/201307/22/0d85672feb4cea05c8d65eac.jpg_350x240_478bfa4a.jpg', 'http://img1.qunarzz.com/sight/p0/201405/22/4f77d372ab47b77eea2605e8db34119e.jpg_350x240_9aa06c0a.jpg', 'http://img1.qunarzz.com/sight/p0/1508/8d/ca6b34f5184fc40897e0896f61910b68.water.jpg_350x240_1e99f600.jpg', 'http://img1.qunarzz.com/sight/p0/1508/cc/a00e22eafcf3265a5d9b3aecd1e4a440.water.jpg_350x240_07ebbfe3.jpg', 'http://img1.qunarzz.com/sight/p0/1508/59/67aee992a0c0789d4cc931130e260533.water.jpg_350x240_4a7339c8.jpg', 'http://img1.qunarzz.com/sight/p0/1508/96/4944b33f82b3984cbeec46e139ffbe95.water.jpg_350x240_f09b90d7.jpg', 'http://img1.qunarzz.com/sight/p0/1508/eb/9c04475b89a9ce068e3550abe4d7d38b.water.jpg_350x240_dd85fbe1.jpg', 'http://img1.qunarzz.com/sight/p0/1508/83/6b5cbc50a06106682f66049cbf1e1b10.water.jpg_350x240_466ff90e.jpg']
    }
  },
  methods: {
    handleListShow () {
      this.showList = true
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
