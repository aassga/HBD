<template lang="pug">
  div.mt-4.mb-4
    b-navbar(type='light' variant='light')
      b-navbar-nav
        b-nav-item(href='#') 團體旅遊
        b-nav-item(href='#') 自由行
        b-nav-item(href='#') 機票
        b-nav-item(href='#') 國內訂房
        //  Navbar dropdowns 
        b-nav-item-dropdown(text='玩咖推薦' right)
          b-dropdown-item.small(href='#') 精選住宿
          b-dropdown-item.small(href='#') 好食餐卷
</template>
<script>
export default {
  data() {
    return {
      
    }
  },
}
</script>

<style lang="sass" scoped>
  .small
    font-size: 90%!important
</style>
