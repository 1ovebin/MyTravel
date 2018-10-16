<template>
  <div class="gallery-container">
    <div class="gallery-header">
      <span class="iconfont back-icon" @click="back">&#xe624;</span>
      <h3 class="gallery-title">景区图片</h3>
    </div>
    <ul class="gallery-list" >
      <li v-for="(item, index) of galleryList" :key="index">
        <img :src="item" @click="handleGallaryShow">
      </li>
      <div class="clear"></div>
    </ul>
    <swiper-gallery :imgArr="imgArr" v-show="showGallary" @close="handleGallaryClose"></swiper-gallery>
  </div>
</template>

<script>
import SwiperGallery from '@/components/SwiperGallery'
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
  components: {
    SwiperGallery
  },
  data () {
    return {
      showGallary: false,
      imgArr: ['http://img1.qunarzz.com/sight/p0/1411/20/127428acf46f1d895892b642c7431e95.water.jpg_r_800x800_98dff97e.jpg', 'http://img1.qunarzz.com/sight/p0/1411/11/ef2d383589ab4a04f46117fd8357f09f.water.jpg_r_800x800_878c63cb.jpg']
    }
  },
  methods: {
    back () {
      this.$router.go(-1)
    },
    handleGallaryShow () {
      this.showGallary = true
    },
    handleGallaryClose () {
      this.showGallary = false
    }
  }
}
</script>

<style scoped>
  .gallery-container{
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    min-height: 100%;
    background: #f5f5f5;
  }
  .gallery-header{
    position: fixed;
    width: 100%;
    height: .88rem;
    background: #fff;
    z-index: 91;
    border-bottom: 1px solid #e0e0e0;
  }
  .gallery-title{
    overflow: hidden;
    margin: 0 1rem;
    line-height: .88rem;
    white-space: nowrap;
    text-overflow: ellipsis;
    font-size: .32rem;
    text-align: center;
    color: #333;
  }
  .back-icon{
    position: absolute;
    left: 0;
    top: 0;
    width: .8rem;
    height: .88rem;
    line-height: .88rem;
    font-size: .4rem;
    color: #333;
    text-align: center;
    font-weight: bold;
  }
  .gallery-list{
    padding: 1.08rem .2rem .4rem .2rem;
    zoom: 1;
    overflow: hidden;
  }
  .gallery-list li{
    width: 50%;
    float: left;
    margin-bottom: .1rem;
    box-sizing: border-box;
  }
  .gallery-list li img{width: 100%;}
  .gallery-list li:nth-child(even) {
    padding-left: .05rem;
  }
  .gallery-list li:nth-child(odd) {
    padding-right: .05rem;
  }
</style>
