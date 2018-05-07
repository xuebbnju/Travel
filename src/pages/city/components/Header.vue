<template>
<div class="header">
城市选择
  <router-link to='/'>
    <div class="iconfont header-back">&#xe624;</div>
  </router-link>
</div>
</template>
<script >
export default {
  name: 'CityHeader'
}
</script>
<style lang="stylus" scoped>
@import "~style/varibles.styl"
.header
  overflow: hidden
  position: relative
  height: $headerHeight
  line-height: $headerHeight
  text-align: center
  color: #fff
  background-color: $bgColor
  font-size: .32rem
  .header-back
    width: .64rem
    text-align: center
    font-size: .4rem
    position: absolute
    left: 0
    top: 0
    color: #fff
</style>
