<template lang="pug">
  div
    b-navbar(type='light' variant='white')
      b-navbar-nav(v-for="(item,i) in trip" :key="item.trip")
        b-nav-item.small.pl-2.font-weight-bold(href='#') {{ item.traval }}
        b-nav-item.small.pl-2.font-weight-bold(href='#') {{ item.free }}
        b-nav-item.small.pl-2.font-weight-bold(href='#') {{ item.air }}
        b-nav-item.small.pl-2.font-weight-bold(href='#') {{ item.check }}
        b-nav-item-dropdown.small.pl-2.font-weight-bold(text='玩咖推薦' lrft)
          b-dropdown-item.small.pl-2.font-weight-bold(href='#') {{ item.motel }}
          b-dropdown-item.small.pl-2.font-weight-bold(href='#') {{ item.eat }}

</template>
<script>
export default {
  data() {
    return {
      trip:[
        {
          traval:'關於我們',
          free:'官方部落格',
          air:'服務條款',
          check:'隱私權政策',
          motel:'免責聲明',
          eat:'公司公告',
        }
      ],
    }
  },
}
</script>

<style lang="sass" scoped>
  .small
    font-size: 90%!important
</style>
