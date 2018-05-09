<template>
<div>
  <div class="banner">
    <img src="http://img1.qunarzz.com/sight/p0/1411/13/0cd5a9a57ae0d1b9b935ec604ce0f9bf.water.jpg_600x330_d6101489.jpg" alt="" class="banner-img">
    <div class="banner-info">
      <div class="banner-title">南京海底世界</div>
      <div class="banner-number"><span class="iconfont banner-icon" @click="handelBannerClick">&#xe692;</span> 39</div>
    </div>
  </div>
  <common-gallary :imgs="imgs" v-show="showGallary" @close="handleGallaryClose"></common-gallary>
</div>
</template>
<script >
import CommonGallary from 'common/gallary/Gallary.vue'
export default {
  name: 'DetailBanner',
  components: {
    CommonGallary
  },
  data () {
    return {
      imgs: ['http://img1.qunarzz.com/sight/p0/1706/f8/f88683e4a602c7c3a3.img.jpg_r_800x800_e18b3f15.jpg', 'http://img1.qunarzz.com/sight/p0/1706/9b/9b6ce141d1a23b30a3.img.jpg_r_800x800_24dbd8cb.jpg'],
      showGallary: false
    }
  },
  methods: {
    handelBannerClick () {
      this.showGallary = true
    },
    handleGallaryClose () {
      this.showGallary = false
    }
  },
  mounted () {}
}
</script>
<style lang='stylus' scoped>
.banner
    position: relative
    overflow: hidden
    height: 0
    padding-bottom: 55%
    .banner-img
      width: 100%
    .banner-info
      display: flex
      position: absolute
      left: 0
      right: 0
      bottom: 0
      line-height: .6rem
      color: #fff
      background-image: linear-gradient(top, rgba(0, 0, 0, 0), rgba(0, 0, 0, 0.8))
      .banner-title
        flex: 1
        font-size: .32rem
        padding: 0 .2rem
      .banner-number
        height: .32rem
        line-height: .32rem
        margin-top: .14rem
        padding: 0 .4rem
        border-radius: .2rem
        background: rgba(0, 0, 0, .8)
        font-size: .24rem
        .banner-icon
          font-size: .24rem
</style>
