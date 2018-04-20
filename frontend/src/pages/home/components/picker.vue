<template>
  <div>
    <div class="picker-nav">
      <div :class="{'nav-tab':true, active: currentTab === 'tabJieji'}" @click="toggleTab('tabJieji')">接机</div>
      <div :class="{'nav-tab':true, active: currentTab === 'tabSongji'}" @click="toggleTab('tabSongji')">送机</div>
    </div>
    <div class="picker-content">
      <div :is="currentTab" keep-alive></div>
    </div>
  </div>
</template>

<script>
import TabJieji from './picker_component/tab-jieji.vue'
import TabSongji from './picker_component/tab-songji.vue'
export default {
  name: 'picker',
  data () {
    return {
      currentTab: 'tabJieji'
    }
  },
  components: {
    TabJieji,
    TabSongji
  },
  methods: {
    toggleTab: function (tab) {
      this.currentTab = tab
    }
  }
}
</script>

<style lang="stylus" scoped>
.picker-nav
  display flex
  width 100%
  background #eee
  .active
    background #fff
  .nav-tab
    padding .6em .2em
    font-size 1.2em
    font-weight bold
    flex-grow 2
    text-align center
    height 100%

</style>
