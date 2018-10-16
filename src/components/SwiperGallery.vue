<template>
  <div class="imgSwiper-container" @click="handleGallaryClick">
    <div class="imgSwiper-box">
      <swiper :options="swiperOptions">
        <swiper-slide v-for="(item, index) of imgArr" :key="index">
          <img :src="item">
        </swiper-slide>
        <div class="swiper-pagination" slot="pagination"></div>
      </swiper>
    </div>
  </div>
</template>

<script>
export default {
  name: 'SwiperGallery',
  props: {
    imgArr: Array
  },
  data () {
    return {
      swiperOptions: {
        pagination: '.swiper-pagination',
        paginationType: 'fraction',
        observeParents: true,
        observer: true
      }
    }
  },
  methods: {
    handleGallaryClick () {
      this.$emit('close')
    }
  }
}
</script>

<style scoped>
  .imgSwiper-container >>> .swiper-container{
     overflow: inherit
  }
  .imgSwiper-container{
    display: flex;
    flex-direction: column;
    justify-content: center;
    overflow: hidden;
    position: fixed;
    z-index: 99;
    top: 0;
    bottom: 0;
    width: 100%;
    background-color: #000;
  }
  .imgSwiper-box{
    height: 0;
    width: 100%;
    padding-bottom: 62.5%;
  }
  .imgSwiper-box img{width: 100%;}
  .swiper-pagination{color: #fff;bottom: -1rem;}
</style>
