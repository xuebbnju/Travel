<template>
<div class="wrapper">
  <swiper :options="swiperOption" >
    <swiper-slide v-for="item of swiperList" :key="item.id">
      <img class="swiper-img" :src="item.imgUrl">
    </swiper-slide>
    <div class="swiper-pagination"  slot="pagination"></div>
  </swiper>
</div>
</template>
<script >
export default {
  name: 'HomeSwiper',
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true
      },
      swiperList: [{
        id: '0001',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1804/77/ad7693460cc4de02.jpg_890x330_112cec66.jpg'
      }, {
        id: '0002',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1804/d5/fb4a5c81cd87a002.jpg_890x330_901edbfc.jpg'
      }]
    }
  }
}
</script>
<style lang="stylus" scoped>
@import "~style/varibles.styl"
.wrapper >>> .swiper-pagination-bullet-active
  background: #fff
.wrapper
  width:100%
  height:0
  overflow: hidden
  padding-bottom: 35%
  .swiper-img
    width:100%
</style>
