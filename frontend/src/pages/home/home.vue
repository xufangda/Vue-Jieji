<template>
  <div class="home">
    <home-header></home-header>
    <!-- <home-icons></home-icons> -->
    <home-picker></home-picker>
  </div>
</template>

<script>
import HomeHeader from './components/header'
import HomePicker from './components/picker'
import HomeIcons from './components/icons'
export default {
  name: 'home',
  components: {
    HomeHeader,
    HomePicker,
    HomeIcons
  }
}
</script>

<style lang="stylus" scoped>
  .home
    font-family "PingFang-SC", "Hiragino Sans GB", "微软雅黑", "Microsoft YaHei", "Heiti SC"
    min-width 6.4rem
</style>
