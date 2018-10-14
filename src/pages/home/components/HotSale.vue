<template>
  <div class="hot-group">
    <div class="group-title">
      <img class="hot-group-img" src="http://img1.qunarzz.com/piao/fusion/1711/16/bfbb9874e8f11402.png">
      <span class="hot-group-title">本周热门榜单</span>
      <a class="hot-group-more" href="javascript:void(0)">全部榜单<span class="iconfont hot-group-icon">&#xe6a7;</span></a>
    </div>
    <ul class="hotsale-list">
      <li class="hotsale-item" v-for="item of hotList" :key="item.id">
        <a class="fulllink" href="#">
          <div class="hotsale-tag" v-if="item.topUrl">
            <img :src="item.topUrl">
          </div>
          <div class="hotsale-imgcon">
            <img :src="item.imgUrl">
          </div>
          <div class="hotsale-sight ellipsis">{{item.hotTitle}}</div>
          <div class="hotsale-price">
            <span class="mpg-price">¥<em class="mpg-price-num">{{item.hotPrice}}</em></span>起
          </div>
        </a>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeHotList',
  props: {
    hotList: Array
  }
}
</script>

<style scoped>
  .hot-group{margin-top: .2rem;background: #ffffff}
  .group-title{padding: .24rem 0 .26rem;position: relative}
  .hot-group-img{display: inline-block;overflow: hidden;width: .3rem;height: .3rem;margin-left: .2rem;vertical-align: top}
  .hot-group-title{margin-left: .08rem;height: .44rem;color: #212121;font-size: .32rem;line-height: .44rem}
  .hot-group-more{position: absolute;top: .36rem;right: .32rem;color: #616161;font-size: .24rem;line-height: .28rem}
  .hot-group-icon{margin-left: .04rem;font-size: .35rem;font-weight: bold;vertical-align: bottom}
  .hotsale-list{padding: 0 .24rem;overflow-x: scroll;white-space: nowrap;}
  .hotsale-item{position: relative;display: inline-block;padding: .06rem 0 .2rem;width: 2rem;}
  .hotsale-item:not(:first-child) {margin-left: .12rem;}
  .fulllink {display: block;width: 100%;height: 100%;}
  .hotsale-tag{position: absolute;top: 0;left: 0;z-index: 1;overflow: hidden;width: .84rem;height: .4rem;}
  .hotsale-tag img{width: 100%}
  .hotsale-imgcon{overflow: hidden;width: 2rem;height: 0;padding-bottom: 100%;background: #f0f5f8;}
  .hotsale-imgcon img{width: 100%;}
  .hotsale-sight {margin-top: .12rem;color: #212121;font-size: .24rem;line-height: .32rem;text-align: center;}
  .ellipsis {overflow: hidden;width: 100%;white-space: nowrap;text-overflow: ellipsis;}
  .hotsale-price {color: #616161;font-size: .24rem;line-height: .36rem;text-align: center;}
  .hotsale-price .mpg-price {color: #ff8300;}
  .hotsale-price .mpg-price-num {font-size: .28rem;}
</style>
