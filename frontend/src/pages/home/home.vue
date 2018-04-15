<template>
  <div>
    <home-header></home-header>
    <!-- <home-picker></home-picker> -->
  </div>
</template>

<script>
import HomeHeader from './components/header'
import HomePicker from './components/picker'
export default {
  name: 'home',
  components: {
    HomeHeader,
    HomePicker
  }
}
</script>

<style lang="stylus" scoped>
body
  font-family "PingFang-SC", "Hiragino Sans GB", "微软雅黑", "Microsoft YaHei", "Heiti SC"
</style>
