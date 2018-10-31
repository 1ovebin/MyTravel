<template>
  <ul class="special-container">
    <li class="special-item item-border-right" v-for="item of specList" :key="item.id" :style="{backgroundImage:'url(' + item.imgUrl + ')'}"></li>
    <div class="clear"></div>
  </ul>
</template>

<script>
export default {
  name: 'HomeSpecial',
  props: {
    specList: Array
  }
}
</script>

<style scoped>
  .special-container{width: 100%;margin-top: .2rem;background-color: #fff;}
  .special-item{float: left;box-sizing: border-box;width: 50%;height: 1.4rem;line-height: 1.4rem;background-repeat: no-repeat;background-position: center center;background-size: auto 100%}
  .item-border-right{border-right: 1px solid #F5F5F5;}
</style>
