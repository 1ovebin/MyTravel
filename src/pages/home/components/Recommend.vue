<template>
  <div class="re-group">
    <div class="re-group-title">
      <img class="re-title-img" src="http://img1.qunarzz.com/piao/fusion/1711/89/ebc329f16c55bb02.png">
      <span class="re-title">猜你喜欢</span>
    </div>
    <ul class="re-like-list">
      <li class="re-like-item" v-for="item of recoList" :key="item.id">
        <div class="re-like-imgcon">
          <img class="re-like-img" :src="item.imgUrl">
          <span class="re-like-tag" :style="{backgroundImage:'url(' + item.imgBg + ')'}">{{item.reTag}}</span>
        </div>
        <div class="re-like-info">
          <div class="re-like-title re-ellipsis">{{item.reTitle}}</div>
          <div class="re-like-comment">
            <span class="ref-starlevel">
              <strong class="iconfont ref-starlevel-gain" :style="{width:item.Evaluate}">&#xe81b;&#xe81b;&#xe81b;&#xe81b;&#xe81b;</strong>
              <span class="iconfont ref-starlevel-total">&#xe81b;&#xe81b;&#xe81b;&#xe81b;&#xe81b;</span>
            </span>
            <span class="re-comment-num">{{item.reCommentNum}}条评论</span>
          </div>
          <div class="re-like-price">
            <span class="reg-price">¥<em class="reg-price-num">{{item.rePrice}}</em></span>起
            <span class="re-like-address">{{item.reAddress}}</span>
          </div>
          <div class="re-like-feature" v-if="item.reEllipsis">
            <div class="re-ellipsis2">{{item.reEllipsis}}</div>
          </div>
        </div>
      </li>
    </ul>
    <a class="re-like-more" href="javascript:void(0)">查看所有产品</a>
  </div>
</template>

<script>
export default {
  name: 'HomeRecommend',
  props: {
    recoList: Array
  }
}
</script>

<style scoped>
  .re-group{margin-top: .2rem;background: #ffffff;}
  .re-group-title{position: relative;padding: .24rem 0 .26rem}
  .re-title-img{display: inline-block;overflow: hidden;width: .3rem;height: .3rem;margin-left: .2rem;vertical-align: text-top}
  .re-title{display: inline-block;margin-left: .08rem;height: .44rem;color: #d62727;font-size: .32rem;line-height: .44rem}
  .re-like-list{margin-left: .24rem}
  .re-like-item{position: relative;overflow: hidden;padding: .2rem 0;border-bottom: 1px solid #e0e0e0}
  .re-like-imgcon{position: relative;float: left;overflow: hidden;width: 2rem;height: 2rem;background: #f0f5f8}
  .re-like-img{width: 100%}
  .re-like-tag{position: absolute;top: 0;left: 0;width: 1.1rem;height: .38rem;background-size: 100%;color: #fff;font-size: .2rem;line-height: .38rem;text-indent: .04rem}
  .re-like-info{overflow: hidden;padding-left: .22rem}
  .re-like-title{margin-top: .26rem;height: .44rem;color: #212121;font-size: .32rem;line-height: .44rem}
  .re-ellipsis{overflow: hidden;width: 100%;white-space: nowrap;text-overflow: ellipsis;}
  .re-like-comment{margin-top: .14rem;height: .34rem}
  .ref-starlevel{display: inline-block;position: relative;width: 1.6rem;height: .28rem;line-height: .28rem;font-size: .28rem;letter-spacing: .02rem;-webkit-transform: scale(.83);-moz-transform: scale(.83);-ms-transform: scale(.83);-o-transform: scale(.83);transform: scale(.83);-webkit-transform-origin: 0 0;-moz-transform-origin: 0 0;-ms-transform-origin: 0 0;-o-transform-origin: 0 0;transform-origin: 0 0}
  .ref-starlevel-gain{z-index: 2;color: #ffb436;overflow: hidden;position: absolute;top: .04rem;left: 0;height: .28rem}
  .ref-starlevel-total{z-index: 1;color: #e0e0e0;overflow: hidden;position: absolute;top: .04rem;left: 0;height: .28rem}
  .re-like-price{position: relative;margin-top: .22rem;color: #616161;font-size: .24rem;line-height: .4rem;}
  .reg-price{color: #ff8300;}
  .reg-price-num{font-size: .4rem}
  .mpg-price{position: absolute;right: .24rem;bottom: 0}
  .re-like-address{position: absolute;right: .24rem;bottom: 0;}
  .re-like-feature{display: inline-block;margin-top: .48rem;margin-right: .24rem;background: #fff9f9;padding: .04rem .1rem;color: #f55;font-size: .24rem;line-height: .34rem;}
  .re-ellipsis2{display: -webkit-box;overflow: hidden;text-overflow: ellipsis;-webkit-line-clamp: 2;-webkit-box-orient: vertical;}
  .re-like-more{display: block;padding: .2rem 0;color: #00afc7;font-size: .28rem;line-height: .4rem;text-align: center;}
</style>
