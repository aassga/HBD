<template lang="pug">
  div.mt-4
    b-navbar(type='white' variant='white')
      b-navbar-nav
        b-nav-item.small.pl-2(href='#') {{ traval }}
        b-nav-item.small.pl-2(href='#') {{ free }}
        b-nav-item.small.pl-2(href='#') {{ air }}
        b-nav-item.small.pl-2(href='#') {{ check }}
        //  Navbar dropdowns 
        b-nav-item-dropdown.small.pl-2(text='玩咖推薦' lrft)
          b-dropdown-item.small.pl-2(href='#') {{ motel }}
          b-dropdown-item.small.pl-2(href='#') {{ eat }}

</template>
<script>
export default {
  data() {
    return {
      traval:'關於我們',
      free:'官方部落格',
      air:'服務條款',
      check:'隱私權政策',
      motel:'免責聲明',
      eat:'公司公告',
    }
  },
}
</script>

<style lang="sass" scoped>
  .small
    font-size: 90%!important
  .navbar-nav
    .nav-link
      color:#F60 
</style>
