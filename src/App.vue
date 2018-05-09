<template>
<div id="app">
  <keep-alive excloude="Detail">
    <router-view/>
  </keep-alive>
</div>
</template>
<script>
export default {
  name: 'App'
}
</script>
<style>
</style>
