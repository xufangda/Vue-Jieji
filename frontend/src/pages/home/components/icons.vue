<template>
  <div class='icons'>
    <swiper :options='swiperOption'>
      <!-- slides -->
      <swiper-slide v-for='page of pages' :key='page.index'>
        <div
          class='icon'
          v-for='item of page'
          :key='item.id'
        >
          <div class='icon-img'>
            <img class='icon-img-content' :src='item.imgUrl'>
          </div>
          <p class='icon-desc'>{{item.desc}}</p>
        </div>
      </swiper-slide>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeIcons',
  data () {
    return {
      swiperOption: {
        autoplay: false
      },
      iconList: [{
        id: '0001',
        imgUrl: require('styles/icons/pick.png'),
        desc: '接机/送机'
      }, {
        id: '0002',
        imgUrl: require('styles/icons/friend.png'),
        desc: '结伴出行'
      }, {
        id: '0003',
        imgUrl: require('styles/icons/moving.png'),
        desc: '搬家用车'
      }, {
        id: '0004',
        imgUrl: require('styles/icons/translate.png'),
        desc: '商务翻译'
      }
      ]
    }
  },
  computed: {
    pages () {
      const pages = []
      this.iconList.forEach((item, index) => {
        const page = Math.floor(index / 4)
        if (!pages[page]) {
          pages[page] = []
        }
        pages[page].push(item)
      })
      return pages
    }
  }
}
</script>

<style lang='stylus' scoped>
@import '~styles/varibles.styl'
@import '~styles/mixins.styl'
.icons >>>.swiper-container
  height: 0
  padding-bottom: 25%
.icons
  min-width 6.2rem
  margin-top:.1rem
  .icon
    height : 0
    position: relative
    overflow: hidden
    float: left
    width: 25%
    padding-bottom:25%
    .icon-img
      position:absolute
      top: 0
      left: 0
      right: 0
      bottom: .44rem
      box-sizing:border-box
      padding: .1rem
      .icon-img-content
        display: block
        margin: 0 auto
        height: 100%
    .icon-desc
      position: absolute
      left: 0
      right: 0
      bottom:0
      height : .44rem
      line-height : .44rem
      setFontfamily()
      font-weight bold
      color: $darkTextColor
      text-align: center
      ellipsis()
</style>
