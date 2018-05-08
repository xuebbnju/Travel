<template>
<div>
  <div class="search">
  <input type="text" placeholder="输入城市名或拼音" class="search-input" v-model="keyword">
</div>
<div class="search-content" ref="search" v-show="keyword">
  <ul>
    <li v-for="item of list" :key="item.id" class="search-item border-bottom" @click="handleCityClick(item.name)">{{item.name}}</li>
    <li v-show="hasNoData" class="search-item border-bottom">没有找到匹配数据</li>
  </ul>
</div>
</div>
</template>
<script >
import Bscroll from 'better-scroll'
import {mapMutations} from 'vuex'
export default {
  name: 'CitySearch',
  props: {
    cities: Object
  },
  data () {
    return {
      keyword: '',
      list: [],
      timer: null
    }
  },
  methods: {
    handleCityClick (city) {
      this.changeCity(city)
      this.$router.push('/')
    },
    ...mapMutations(['changeCity'])
  },
  computed: {
    hasNoData () {
      return !this.list.length
    }
  },
  mounted () {
    this.scroll = new Bscroll(this.$refs.search)
  },
  watch: {
    keyword () {
      if (this.timer) {
        clearTimeout(this.timer)
      }
      if (!this.keyword) {
        this.list = []
        return
      }
      this.timer = setTimeout(() => {
        const result = []
        for (let i in this.cities) {
          this.cities[i].forEach((value) => {
            if (value.spell.indexOf(this.keyword) > -1 || value.name.indexOf(this.keyword) > -1) {
              result.push(value)
            }
          })
        }
        this.list = result
      }, 100)
    }
  }
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
.search-content
  position: absolute
  top: 1.5rem
  left: 0
  bottom: 0
  right: 0
  z-index: 1
  background: #eee
  .search-item
    line-height: .62rem
    padding-left: .2rem
    color: #666
    background: #fff
</style>
