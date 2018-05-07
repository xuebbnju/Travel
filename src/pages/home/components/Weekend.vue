<template>
<div class="">
  <div class="title">周末去哪儿</div>
  <ul>
    <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
      <div class="item-img-wrapper">
        <img class="item-img" :src="item.imgUrl" alt="">
      </div>
      <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
      </div>
    </li>
  </ul>
</div>
</template>
<script >
export default {
  name: 'HomeWeekend',
  data () {
    return {
      recommendList: [{
        id: '0001',
        title: '南京汤山',
        desc: '享受特色温泉“冷雾温泉”，感受冰凉体验',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1505/f3/d51669250308cc.jpg_r_640x214_7a127cd0.jpg'
      }, {
        id: '0002',
        title: '南京汤山',
        desc: '享受特色温泉“冷雾温泉”，感受冰凉体验',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1505/f3/d51669250308cc.jpg_r_640x214_7a127cd0.jpg'
      }, {
        id: '0003',
        title: '南京汤山',
        desc: '享受特色温泉“冷雾温泉”，感受冰凉体验',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1505/f3/d51669250308cc.jpg_r_640x214_7a127cd0.jpg'
      }]
    }
  }
}
</script>
<style lang="stylus" scoped>
@import "~style/mixins.styl"
.title
  margin-top: .2rem
  line-height: .8rem
  background: #eee
  text-indent: .2rem
.item-img-wrraper
  height: 0
  width: 100%
  overflow: hidden
  padding-bottom: 33%
  .item-img
    width: 100%
.item-info
  padding: .1rem
  min-width: 0
  .item-title
    line-height: .54rem
    font-size: .32rem
    ellipsis()
  .item-desc
    line-height: .4rem
    color: #ccc
    ellipsis()
  </style>
