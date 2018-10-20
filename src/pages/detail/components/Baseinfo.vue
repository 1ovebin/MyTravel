<template>
  <div class="detail-baseinfo">
    <div class="flex-card">
      <div class="flex-item flexlink-con">
        <a class="card-link" href="javascript:void(0)"></a>
      </div>
      <div class="flex-item"></div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'DetailBaseinfo'
}
</script>

<style scoped>
  .detail-baseinfo{position: relative;top: -.1rem;padding: .1rem .2rem 0 .2rem;margin-bottom: .1rem;background: #fff;-webkit-border-radius: .1rem .1rem 0 0;-moz-border-radius: .1rem .1rem 0 0;border-radius: .1rem .1rem 0 0;}
  .flex-card{display: -webkit-box;display: -moz-box;display: -webkit-flex;display: -moz-flex;display: -ms-flexbox;display: flex;width: 100%;padding-top: .1rem;padding-bottom: .2rem;}
  .flex-item{-webkit-box-flex: 1;-moz-box-flex: 1;-webkit-flex: 1;-moz-flex: 1;-ms-flex: 1;flex: 1;}
  .flexlink-con{position: relative;}
  .card-link{position: absolute;left: 0;top: 0;width: 100%;height: 100%;}
</style>
