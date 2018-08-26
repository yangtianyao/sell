<template>
  <div id="app">
    <v-header v-bind:seller="seller"></v-header>
    <div class="tab">
      <div class="tab-item">
        <router-link to="/goods">商品</router-link>
      </div>
      <div class="tab-item">
        <router-link to="/ratings">评价</router-link>
      </div>
      <div class="tab-item">
        <router-link to="/seller">商家</router-link>
      </div>
    </div>
    <router-view></router-view>
  </div>
</template>

<script type="text/ecmascript-6">
  import header from './components/header/header'

  export default {
    name: 'App',
    components: {
      'v-header': header
    },
    data: function () {
      return {
        seller: {}
      }
    },
    created: function () {
      this.$http.get('/api/seller').then(res => {
        this.seller = res.body.data
      })
    }
  }
</script>

<style lang="stylus" rel="stylesheet/stylus">
  #app
    .tab
      display: flex
      height: 40px
      line-height: 40px
      border-bottom: 1px solid rgba(7, 17, 27, 0.1)
      box-sizing: border-box
      .tab-item
        flex: 1
        width: 100%
        text-align: center
        & > a
          display: block
          font-size: 14px
          color: rgb(77, 85, 93)
          &.router-link-active
            color: red
</style>
