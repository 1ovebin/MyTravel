<template>
  <!-- 推荐 -->
  <div class="mp-promote" style="height: 10rem;">
    <h3 class="mp-ticket-type mpf-border-bottom">去哪儿推荐</h3>
    <div class="mp-ticket-item mp-flexbox mp-border-top">
      <div class="mp-ticket-main mp-flexbox-layout">
      <div>
        <h6 class="mp-ticket-title mp-ellipsis2">【随买随用】济南千佛山成人票</h6>
        <ul class="mp-ticket-light">
          <span class="mp-ticket-desctag">
            <img class="mp-ticket-tagicon" src="https://img1.qunarzz.com/piao/fusion/1804/94/3537f6969acc0c02.png">
            16:55前随买随用
          </span>
        </ul>
        <ul class="mp-ticket-labelcon">
          <span class="mp-ticket-label mp-border mp-label14">
            <img class="mp-ticket-tagicon" src="https://img1.qunarzz.com/piao/fusion/1804/b0/c3cf2897c74ecc02.png">
            自营
          </span>
          <span class="mp-ticket-label mp-border mp-label14">随时退</span>
        </ul>
        <!-- <div class="mp-ticket-supplier">
          <span>去哪儿直销</span>
          <span class="mp-ticket-infobtn mp-border-left">预订须知</span>
          <span class="mpg-iconfont">F</span>
        </div> -->
        <div class="mp-ticket-detail"></div>
      </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'DetailRecommend'
}
</script>

<style>
  /* 推荐 */
  .mp-promote {position: relative;background: #fff;margin-bottom: .2rem;padding-left: .2rem;}
  .mp-promote .mp-ticket-type {background: url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAADAAAAAwCAMAAABg3Am1AAAAflBMVEUAAAD/bm7/b2//b2//eXn/b2//b2//bm7/b2//b2//bm7/b2//b2//b2//bm7/b2//b2//cXH/eHj/qqr/bm7/////cXH/iIj/oqL//f3/mJj/fHz/9/f/8PD/4eH/ycn/6+v/1dX/0ND/t7f/ra3/kpL/jo7/c3P/5ub/vr7o37bEAAAAFHRSTlMA9uZeCfny7NvLt6+PfGZONxsRA/pz1k8AAAFrSURBVEjHpZbZdoMwDERtMEvYE8YJZN/b/v8PNvicJsiYqJzcB548WGNZksUAVWZJHAVBFCdZqQTDwk8lesjUX4hxVB5iQJiPbVMXHpx4RS0czGcYZTYXAyoPb/AqYeFLvEX61nqwEEUlwSKrnl9X/JtmZfl4Oq9d53Pfan2yzurvdAs42OsHaxAKYVDOA207wcEKShlBDhfaIUBu7lsIl2UjuIASLkZTsDaCxpWMFC7ORrCBRfqw7MxZY9Z/w0YqUWLI8tLqJ+25n8BSZP3Am+aG2/Vw1IQ9XmQiwZNV9z+0mkKtJCKmAg094IgXsYg4Ab0gkQh4wRUvgv8I1kTAh7QHCYk3fQIxnbCCHXokImMFPyCJKznB9gvkaijJ7XCnl0+kU3ZISQFttp3DnWW5oQVES3S57D4Eq0RJE+DJSZvh8RRpZDwFaZU8s5o0YxZvPrXdTx0on40sfih+Nnb5wT7x6fDR42Ty8+cXnHyOvDgQEbUAAAAASUVORK5CYII=);background-repeat: no-repeat;background-size: .36rem .36rem;background-position: 0 center;text-indent: .36rem;}
  .mp-ticket-type {overflow: hidden;position: relative;z-index: 4;margin-bottom: -.02rem;padding: 0 .2rem;height: .88rem;background: #fff;color: #333;font-size: .32rem;line-height: .88rem;text-indent: .4rem;}
  .mpf-border-bottom {border-bottom: 1px solid #F3F3F3;}
  /* items */
  .mp-promote .mp-ticket-item {padding: .2rem .2rem .24rem 0;}
  .mp-ticket-item { -webkit-box-sizing: border-box;-moz-box-sizing: border-box;box-sizing: border-box;padding: .2rem;}
  .mp-flexbox {display: -webkit-box;display: -moz-box;display: -webkit-flex;display: -moz-flex;display: -ms-flexbox;display: flex;width: 100%;}
  .mp-ticket-main {-webkit-box-flex: 2.92;-moz-box-flex: 2.92;box-flex: 2.92;-webkit-flex: 2.92;-moz-flex: 2.92;-ms-flex: 2.92;flex: 2.92;}
  .mp-ticket-main, .mp-ticket-side {display: -webkit-box;display: -moz-box;display: -webkit-flex;display: -moz-flex;display: -ms-flexbox;display: flex;-ms-flex-align: center;-webkit-align-items: center;-webkit-box-align: center;align-items: center;}
  .mp-flexbox-layout {width: .02rem;}
  .mp-promote .mp-ticket-title, .mp-promote .mp-ticket-onedaytitle {margin-right: .1rem;line-height: .52rem;padding: 0;font-size: .3rem;}
  .mp-ticket-title, .mp-ticket-onedaytitle {color: #616161;font-size: .28rem;line-height: .4rem;}
  .mp-ellipsis2 {display: -webkit-box;overflow: hidden;text-overflow: ellipsis;-webkit-line-clamp: 2;-webkit-box-orient: vertical;}
  .mp-promote .mp-ticket-light {overflow: hidden;}
  .mp-ticket-desctag .mp-ticket-tagicon, .mp-ticket-label .mp-ticket-tagicon {display: inline-block;width: .2rem;max-height: .32rem;margin-right: .04rem;vertical-align: 0;}
  .mp-ticket-desctag {display: inline-block;height: .32rem;color: #616161;font-size: .24rem;line-height: .32rem;white-space: nowrap;}
  .mp-ticket-label:not(:last-child) {margin-right: .1rem;}
  .mp-ticket-label {display: inline-block;margin-top: .08rem;padding: 0 .04rem;height: .32rem;color: #00afc7;font-size: .2rem;line-height: .32rem;white-space: nowrap;}
  .mp-ticket-label.mp-border::before {border-color: #a5e4ec;border-radius: .08rem;}
  .mp-border::before {-webkit-box-sizing: border-box;-moz-box-sizing: border-box;box-sizing: border-box;top: 0;left: 0;height: 100%;width: 100%;border: 1px solid #e0e0e0;-webkit-transform-origin: 0 0;-moz-transform-origin: 0 0;-ms-transform-origin: 0 0;-o-transform-origin: 0 0;transform-origin: 0 0;}
  .mp-ticket-main, .mp-ticket-side {display: -webkit-box;display: -moz-box;display: -webkit-flex;display: -moz-flex;display: -ms-flexbox;display: flex;-ms-flex-align: center;-webkit-align-items: center;-webkit-box-align: center;align-items: center;}
  .mp-ticket-link {-webkit-box-sizing: border-box;-moz-box-sizing: border-box;box-sizing: border-box;display: block;width: 100%;padding-left: .2rem;}
</style>
