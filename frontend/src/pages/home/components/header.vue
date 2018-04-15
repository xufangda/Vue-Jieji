<template>
  <div class="header">
    <div class="header-bg">
      <img class="header-bg-img" src="https://a0.muscache.com/airbnb/growth/magic_carpet/hero4_medium.jpg">
    </div>
    <div class="header-logo">
      <a class="logo-link" href="/">
      <span class="iconfont logo-icon">&#xe600;</span>
      <span class="logo-font">PickQup</span>
      </a>
    </div>
    <div class="header-slogan">
      <p class="header-slogan-big">PickQup迎你来，全英数万留学生的选择</p>
      <p class="header-slogan-small">伦敦希斯罗，伦敦盖德威克机场现已开放</p>
    </div>
  </div>
</template>

<script>
export default {

}
</script>

<style lang="stylus" scoped>
  .header
    width 100%
    height 4rem
    color #fff
    position relative
    min-width 6.4rem
    .header-bg
      z-index -2
      height 100%
      width 100%
      overflow hidden
      position absolute
      .header-bg-img
        z-index -1
        height auto
        width auto
        min-height 100%
        min-width 100%
        position absolute
        top 50%
        left 50%
        transform translate(-50%, -50%)
    .header-logo
      padding .3rem
      font-size .4rem
      display inline-block
      vertical-align middle
      font-family "PingFang-SC", "Hiragino Sans GB", "微软雅黑", "Microsoft YaHei", "Heiti SC"
      .logo-link, .logo-link:visited
        color: #fff
        .logo-icon
          font-size .6rem
        .logo-font
          font-weight bold

    .header-slogan
      width 100%
      bottom 0
      top 0
      position relative
      background-color rgba(30,30,30,0.1)
      height 2.8rem
      box-sizing border-box
      padding .5rem
      .header-slogan-big
        font-size .5rem
        font-weight 700
      .header-slogan-small
        padding .3rem 0
        font-size .3rem

</style>
