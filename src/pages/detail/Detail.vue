<template>
  <div class="detail-page">
    <detail-banner></detail-banner>
    <detail-header></detail-header>
    <detail-baseinfo></detail-baseinfo>
  </div>
</template>

<script>
import detailBanner from '@/pages/detail/components/Banner'
import detailBaseinfo from '@/pages/detail/components/Baseinfo'
import detailHeader from '@/pages/detail/components/Header'
export default {
  name: 'detail',
  components: {
    detailBanner,
    detailHeader,
    detailBaseinfo
  }
}
</script>

<style scoped>
  .detail-page{background: #f5f5f5;}
</style>
