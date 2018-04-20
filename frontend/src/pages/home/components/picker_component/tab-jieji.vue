<template>
  <div class="jieji">
    <div class="jieji-item">
      <label class="item-label">落地机场</label>
      <input class="item-input border" placeholder="伦敦希斯罗" type="text">
    </div>
    <div class="jieji-item">
      <label class="item-label">目的地</label>
      <input class="item-input border-bottom" placeholder="伦敦 / 雷丁 / 巴斯" type="text">
    </div>
    <div class="jieji-item">
      <label class="item-label">预计日期</label>
      <div class="item-input">
        <date-picker :value="date"></date-picker>
      </div>
    </div>
  </div>
</template>

<script>
import DatePicker from 'vuejs-datepicker'

export default {
  name: 'tabJieji',
  data () {
    return {
      date: new Date()
    }
  },
  components: {
    DatePicker
  }
}
</script>

<style lang="stylus" scoped>

  .jieji
    padding .2rem
    .jieji-item
      padding .1rem 0
      .border-bottom
        color black
      .item-label
        font-size .3rem
        line-height .6rem
        height .6rem
        font-weight bold
      .item-input
        font-size .36rem
        padding .1rem .14rem
        box-sizing border-box
        width 100%
        background white
        border .02rem solid
      .item-input::placeholder
        color #aaa
</style>
