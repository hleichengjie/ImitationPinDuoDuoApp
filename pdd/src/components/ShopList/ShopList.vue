<template>
  <a class="recommend-item">
    <img :src="item.thumb_url" alt="" width="100%" v-if="item.thumb_url">
    <h4 class="item-title">{{item.short_name}}</h4>
    <div class="item-bottom">
      <span class="item-price">￥{{item.price/100}}</span>
      <span class="item-sales">{{item.sales_tip}}</span>
      <button class="item-btn">找相关</button>
    </div>
  </a>
</template>

<script>
    export default {
        name: "ShopList",
      props:{
          item:Object
      }
    }
</script>

<style scoped lang="stylus" ref="stylesheet/stylus">
  .recommend-item:nth-child(2n-1)
    margin-right 1%
  .recommend-item
    width 49.5%
    padding-bottom 15px
    margin-bottom 15px
    background #fff
    .item-title
      height 20px
      overflow hidden
      line-height 20px
      font-size 13px
      font-weight lighter
      margin 5px 0
      padding 0 5px
    .item-bottom
      display flex
      flex-direction row
      align-items center
      padding 0 6px
      .item-price
        flex 2
        font-weight bolder
        color red
        font-size 10px
      .item-sales
        flex 4
        font-size 10px
        color #666
      .item-btn
        flex 2
        height 26px
        border 1px solid orangered
        border-radius 5px
        font-size 10px
        background-color transparent
        color red
</style>
