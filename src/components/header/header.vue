<template>
  <div class="header">
    <div class="header_top">
      <div class="header_top_item seller_img">
        <img src="http://static.galileo.xiaojukeji.com/static/tms/seller_avatar_256px.jpg">
      </div>
      <div class="header_top_item seller_info">
        <div class="title_box">
          <img>
          <span>粥品香坊（回龙观）</span>
        </div>
        <div class="desc_box">
          <span class="desc">蜂鸟专送</span>
          <span>/</span>
          <span class="delivery_time">38</span>
          <span>分钟送达</span>
        </div>
        <div class="supports">
          <div class="support_item supports_left">
            <img>
            <span>在线支付满28减5</span>
          </div>
          <div class="support_item supports_right">
            <a>5</a>
            <span>个</span>
          </div>
        </div>
      </div>
    </div>
    <div class="header_bottom">
      <a>粥品香坊其烹饪粥料的秘方源于中国千年古法，在融和现代制作工艺，由世界烹饪大师屈浩先生领衔研发。坚守纯天然、0添加的良心品质深得消费者青睐，发展至今成为粥类的引领品牌。是2008年奥运会和2013年园博会指定餐饮服务商。</a>
    </div>
  </div>
</template>

<script type="text/ecmascript-6">
  export default {}
</script>

<style lang="stylus" rel="stylesheet/stylus">
  .header
    .header_top
      padding: 20px 20px
      &:after
        clear: both
        content: ''
        display: block
      .seller_img
        width: 20%
        float: left
        & > img
          width: 100%
      .seller_info
        float: right
        width: 77%
        line-height: 25px;
        .supports_left
          float: left
        .supports_right
          float: right
    .header_bottom
      overflow: hidden
      text-overflow: ellipsis
      white-space: nowrap
      width: 94%
      margin: 0 auto
      font-size: 14px;

</style>
