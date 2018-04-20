<template>
  <div class="jieji">
    <div class="jieji-item">
      <label class="item-label ">预计日期</label>
      <div class="item-input">
        <date-picker :value="date"></date-picker>
      </div>
    </div>
    <div class="jieji-item">
      <label class="item-label">起飞机场</label>
      <input class="item-input" placeholder="伦敦希斯罗" type="text">
    </div>
    <div class="jieji-item">
      <label class="item-label">目的地</label>
      <input class="item-input" placeholder="伦敦 / 雷丁 / 巴斯" type="text">
    </div>
    <div class="jieji-item">
      <button class="item-btn">查 询</button>
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
@import '~styles/variables.styl'
  .jieji
    padding .2rem
    .jieji-item
      padding .06rem 0
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
        border-color #ccc
      .item-input::placeholder
        color #aaa
      .item-btn
        text-align center
        font-size .36rem
        margin-top .2rem
        padding .16rem .14rem
        box-sizing border-box
        width 100%
        background $bgColor
        color white
        font-weight bold
        border-radius .1rem
</style>
