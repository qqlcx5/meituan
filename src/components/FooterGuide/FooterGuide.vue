<template>
  <div class="FooterGuide-box">
    <div class="FooterGuide">
      <article
        class="item"
        :class="{ on: '/home' === $route.path }"
        @click="goTo('/home')"
      >
        <i class="iconfont icon-waimai"></i>
        <span>外卖</span>
      </article>
      <article
        class="item"
        :class="{ on: '/search' === $route.path }"
        @click="goTo('/search')"
      >
        <i class="iconfont icon-sousuo1"></i>
        <span>搜索</span>
      </article>
      <article
        class="item"
        :class="{ on: '/order' === $route.path }"
        @click="goTo('/order')"
      >
        <i class="iconfont icon-order"></i>
        <span>订单</span>
      </article>
      <article
        class="item"
        :class="{ on: '/profile' === $route.path }"
        @click="goTo('/profile')"
      >
        <i class="iconfont icon-geren"></i>
        <span>我的</span>
      </article>
    </div>
  </div>
</template>

<script>
export default {
  name: "FooterGuide",
  data() {
    return {};
  },
  methods: {
    goTo(path) {
      this.$router.replace(path);
    }
  }
};
</script>

<style lang="stylus" rel="stylesheet/stylus" scoped>
.FooterGuide-box
  position fixed
  left 0
  right 0
  bottom 0
  .FooterGuide::before
    content ''
    position absolute
    z-index 200
    left 0
    top 0
    width 100%
    height 1px
    background-color #e4e4e4
  .FooterGuide
    position relative
    background-color #fff
    width 100%
    height 1rem
    max-width 750PX
    margin: 0 auto
    display flex
    .item
      display flex
      flex 1
      text-align center
      flex-direction column
      align-items center
      margin 0.1rem
      color #999
      .iconfont
        font-size 0.44rem
      span
        font-size 0.24rem
        margin 0.08rem 0
    .on
      color #02a774
</style>
