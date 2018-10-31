<template>
  <div class="detail-page">
    <detail-banner></detail-banner>
    <detail-header></detail-header>
    <detail-baseinfo></detail-baseinfo>
    <detail-recommend></detail-recommend>
  </div>
</template>

<script>
import detailHeader from '@/pages/detail/components/Header'
import detailBanner from '@/pages/detail/components/Banner'
import detailBaseinfo from '@/pages/detail/components/Baseinfo'
import detailRecommend from '@/pages/detail/components/Recommend'
export default {
  name: 'detail',
  components: {
    detailBanner,
    detailHeader,
    detailBaseinfo,
    detailRecommend
  }
}
</script>

<style scoped>
  .detail-page{background: #f5f5f5;}
</style>
