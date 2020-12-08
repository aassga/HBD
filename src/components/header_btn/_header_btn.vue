<template lang="pug">
  div
    b-navbar(type='light' variant='white')
      b-navbar-nav(v-for="(item,i) in trip" :key="item.trip")
        b-nav-item(href='#' :class="fontmenuObject") {{ item.traval }}
        b-nav-item(href='#' :class="fontmenuObject") {{ item.free }}
        b-nav-item(href='#' :class="fontmenuObject") {{ item.air }}
        b-nav-item(href='#' :class="fontmenuObject") {{ item.check }}
        b-nav-item-dropdown(href='#' :class="fontmenuObject" text='玩咖推薦' left )
          b-dropdown-item(href='#' :class="fontmenuObject") {{ item.motel }}
          b-dropdown-item(href='#' :class="fontmenuObject") {{ item.eat }}

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
          motel:'精選住宿',
          eat:'好食餐卷',
        }
      ],
      fontmenuObject:{
        'small': true, 
        'pl-2': true,
        'font-weight-bold': true,
      },
    }
  },
}
</script>

<style lang="sass" scoped>
  .small
    font-size: 90%!important
</style>
