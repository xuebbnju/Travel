<template>
<div class="search">
  <input type="text" placeholder="输入城市名或拼音" class="search-input">
</div>
</template>
<script >
export default {
  name: 'CitySearch',
  components: {},
  data () {
    return {}
  },
  methods: {},
  mounted () {}
}
</script>
<style lang="stylus" scoped>
@import "~style/varibles.styl"
.search
  height: .72rem
  background: $bgColor
  padding: 0 .1rem
  .search-input
    height: .6rem
    line-height: .6rem
    width: 100%
    text-align: center
    border-radius: .06rem
    color: #666
    box-sizing: border-box
    padding: 0 .1rem
</style>
