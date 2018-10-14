<template>
  <div class="icon-container">
    <swiper :options="swiperOption">
      <swiper-slide v-for="(page, index) of pages" :key="index">
        <div class="icon-items" v-for="item of page" :key="item.id">
          <div class="icon-img">
            <img class="icon-img-content" :src="item.imgUrl">
          </div>
          <p class="icon-desc">{{item.desc}}</p>
        </div>
      </swiper-slide>
      <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeIcons',
  props: {
    iconsList: Array
  },
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        autoplay: false
      }
    }
  },
  computed: {
    pages () {
      const pages = []
      this.iconsList.forEach((item, index) => {
        const page = Math.floor(index / 8)
        if (!pages[page]) {
          pages[page] = []
        }
        pages[page].push(item)
      })
      return pages
    }
  }
}
</script>

<style scoped>
  .icon-container >>> .swiper-container{height: 3.7rem;padding-top: .1rem}
  .icon-container >>> .swiper-pagination-bullet{width: 6px;height: 6px;}
  .icon-container{background: #ffffff;}
  .icon-items{float: left;width: 25%;height: 1.6rem;overflow: hidden}
  .icon-img{width: 1.1rem;height: 1.1rem;margin: .1rem auto 0;}
  .icon-img-content{width: 100%}
  .icon-desc{font-size: .28rem;color: #212121;text-align: center}
</style>
