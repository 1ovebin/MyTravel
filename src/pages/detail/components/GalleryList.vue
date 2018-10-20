<template>
  <div class="gallery-container">
    <div class="gallery-header">
      <span class="iconfont back-icon" @click="back">&#xe624;</span>
      <h3 class="gallery-title">景区图片</h3>
    </div>
    <ul class="gallery-list" >
      <li v-for="(item, index) of galleryList" :key="index">
        <img :src="item" @click="handleGallaryShow" :ShowIndex="index">
      </li>
      <div class="clear"></div>
    </ul>
    <div class="imgSwiper-container" @click="handleGallaryClose" v-show="showGallary">
      <div class="imgSwiper-box">
        <swiper :options="swiperOptions">
          <swiper-slide v-for="item of imgArr" :key="item.id">
            <img :src="item.imgUrl">
          </swiper-slide>
          <div class="swiper-pagination" slot="pagination"></div>
        </swiper>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'gallery',
  props: {
    galleryList: {
      type: Array,
      default () {
        return []
      }
    }
  },
  data () {
    return {
      showGallary: false,
      swiperOptions: {
        pagination: '.swiper-pagination',
        paginationType: 'fraction',
        observeParents: true,
        observer: true
      },
      ShowIndex: '',
      imgArr: [
        {
          id: 0,
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1505/da/da7c46e2eef8714e.water.jpg_r_800x800_67f0539e.jpg'
        },
        {
          id: 1,
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1411/c7/0c38235ff16c8547d539cdf196e09101.water.jpg_r_800x800_a7dc38ec.jpg'
        }
      ]
    }
  },
  methods: {
    back () {
      this.$router.go(-1)
    },
    handleGallaryShow (e) {
      // console.log(e.target.getAttribute('ShowIndex'))
      this.ShowIndex = e.target.getAttribute('ShowIndex')
      console.log(this.ShowIndex)
      this.showGallary = true
    },
    handleGallaryClose () {
      this.showGallary = false
    }
  },
  created () {
    this.$set(this.swiperOptions, 'initialSlide', 0)
  }
}
</script>

<style scoped>
  .imgSwiper-container >>> .swiper-container{overflow: inherit}
  .gallery-container{position: absolute;top: 0;left: 0;width: 100%;min-height: 100%;background: #f5f5f5;}
  .gallery-header{position: fixed;width: 100%;height: .88rem;background: #fff;z-index: 91;border-bottom: 1px solid #e0e0e0;}
  .gallery-title{overflow: hidden;margin: 0 1rem;line-height: .88rem;white-space: nowrap;text-overflow: ellipsis;font-size: .32rem;text-align: center;color: #333;}
  .back-icon{position: absolute;left: 0;top: 0;width: .8rem;height: .88rem;line-height: .88rem;font-size: .4rem;color: #333;text-align: center;font-weight: bold;}
  .gallery-list{padding: 1.08rem .2rem .4rem .2rem;zoom: 1;overflow: hidden;}
  .gallery-list li{width: 50%;float: left;margin-bottom: .1rem;box-sizing: border-box;}
  .gallery-list li img{width: 100%;}
  .gallery-list li:nth-child(even) {padding-left: .05rem;}
  .gallery-list li:nth-child(odd) {padding-right: .05rem;}
  .imgSwiper-container{display: flex;flex-direction: column;justify-content: center;overflow: hidden;position: fixed;z-index: 99;top: 0;bottom: 0;width: 100%;background-color: #000;}
  .imgSwiper-box{height: 0;width: 100%;padding-bottom: 62.5%;}
  .imgSwiper-box img{width: 100%;}
  .swiper-pagination{color: #fff;bottom: -1rem;}
</style>
