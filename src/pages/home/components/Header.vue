<template>
<div class="header">
  <div class="header-left">
    <div class="iconfont back-icon">&#xe624;</div>
  </div>
  <div class="header-input">
    <span class="iconfont ">&#xe632;</span>
    输入城市/景点/游玩主题
  </div>
  <router-link to='/city'>
    <div class="header-right">{{city}}
       <span class="iconfont arrow-icon">&#xe64a;</span>
    </div>
  </router-link>
</div>
</template>
<script >
import {mapState} from 'vuex'
export default {
  name: 'HomeHeader',
  computed: {
    ...mapState(['city'])
  }
}
</script>
<style lang="stylus" scoped>
@import "~style/varibles.styl"
.header
  line-height: $headerHeight
  display: flex
  background-color: $bgColor
  color: #fff
  .header-left
    width: .64rem
    // float: left
    .back-icon
      text-align:center
      font-size:.4rem
  .header-input
    flex:1
    background:#fff
    border-radius:.1rem
    margin-top:.12rem
    height:.64rem
    margin-left:.2rem
    line-height:.64rem
    color:#ccc
    padding-left:.2rem
  .header-right
    color: #fff
    min-width: 1.04rem
    padding: 0 .1rem
    text-align:center
    .arrow-icon
      font-size:.24rem
      margin-left:-.04rem
</style>
