<template>
  <div class="header">
    <div class="background">
      <img :src="seller.avatar"/>
    </div>
    <div class="header_top">
      <div class="header_top_item seller_img">
        <img :src="seller.avatar">
      </div>
      <div class="header_top_item seller_info">
        <div class="title_box">
          <span>品牌</span>
          <span>{{seller.name}}</span>
        </div>
        <div class="desc_box">
          <span class="desc">{{seller.description}}/{{seller.deliveryTime}}分钟送达</span>
        </div>
        <div v-if="seller.supports" class="supports">
          <div class="supports_left">
            <span>减</span>
            <span>{{seller.supports[0].description}}</span>
          </div>
          <div class="supports_right">
            <span>{{seller.supports.length}}个 ></span>
          </div>
        </div>
      </div>
    </div>
    <div class="header_bottom">
      <span>公告</span>
      <span class="bulletin">{{seller.bulletin}}</span>
      <span>></span>
    </div>
  </div>
</template>

<script type="text/ecmascript-6">
  export default {
    props: ['seller']
  }
</script>

<style lang="stylus" rel="stylesheet/stylus">
  .header
    background: rgba(7, 17, 27, 0.5);
    color: #fff;
    font-size: 13px;
    position: relative;
    .background
      width: 100%;
      height: 100%;
      position: absolute;
      z-index: -1;
      filter: blur(10px);
      img
        width: 100%;
        height: 100%;
    .header_top
      padding: 25px 0 0 0
      height: 64px
      margin: 0 0 20px 0
      display: flex
      .seller_img
        margin: 0 10px 0 25px
        & > img
          width: 64px
          vertical-align: top
      .seller_info
        flex-grow: 1
        margin: 0 10px 0 0;
        .title_box
          font-size: 16px;
          margin-bottom: 8px;
        .desc_box
          margin-bottom: 8px;
        .supports
          display: flex
          .supports_left
            flex: 1
          .supports_right
            padding: 6px 8px;
            border-radius: 14px;
            background: rgba(0, 0, 0, 0.2);
    .header_bottom
      font-size: 13px;
      display: flex;
      padding: 8px 12px 8px 9px;
      background: rgba(7, 17, 27, 0.2);
      .bulletin
        flex: 1
        overflow: hidden;
        text-overflow: ellipsis;
        white-space: nowrap;

</style>
