<template>
  <div class="header">
    <div class="header_top">
      <div class="header_top_item seller_img">
        <img src="http://static.galileo.xiaojukeji.com/static/tms/seller_avatar_256px.jpg">
      </div>
      <div class="header_top_item seller_info">
        <div class="title_box">
          <span>品牌</span>
          <span>{{seller.data.name}}</span>
        </div>
        <div class="desc_box">
          <span class="desc">蜂鸟专送/38分钟送达</span>
        </div>
        <div class="supports">
          <div class="supports_left">
            <span>减</span>
            <span>在线支付满28减5</span>
          </div>
          <div class="supports_right">
            <a>5个 ></a>
          </div>
        </div>
      </div>
    </div>
    <div class="header_bottom">
      <span>公告</span>
      <span class="bulletin">{{seller.data.bulletin}}</span>
      <span>></span>
    </div>
  </div>
</template>

<script type="text/ecmascript-6">
  export default {
    props: {
      seller: {
        type: Object
      }
    }
  }
</script>

<style lang="stylus" rel="stylesheet/stylus">
  .header
    .header_top
      height: 64px
      margin: 20px 0
      display: flex
      .seller_img
        margin: 0 10px
        & > img
          width: 64px
          vertical-align: top
      .seller_info
        flex-grow: 1
        margin: 0 10px 0 0;
        .title_box
          font-size: 18px;
          margin-bottom: 8px;
        .desc_box
          font-size: 14px
          margin-bottom: 8px;
        .supports
          font-size: 14px
          display: flex
          .supports_left
            flex: 1
    .header_bottom
      margin: 0px 15px;
      font-size: 14px;
      display: flex
      .bulletin
        flex: 1
        overflow: hidden;
        text-overflow: ellipsis;
        white-space: nowrap;

</style>
