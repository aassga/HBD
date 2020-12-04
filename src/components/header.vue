<template lang="pug">
  header.shadow-sm.mb-5.bg-white.rounded
    section#header
      .container
        .row
          .col-12
            .row.justify-content-center.align-items-center
              .col-sm-5
                img(:src="svg")
              .col-sm-7.row.justify-content-end
                b-nav.font17(v-for="(item,i) in traval" :key="item.traval")
                  b-nav-item.mt-1.font-weight-bold {{ item.cis }}
                  b-nav-item.mt-1.font-weight-bold {{ item.rating }}
                  b-nav-item.mt-1.font-weight-bold {{ item.new }}
                    span.text-warning.pl-2 {{ item.hotnews }}
                  b-nav-item 
                    button.btn.btn-sm.btn-info(type='button') {{ login }}
            headerbtn

</template>
<script>
import headerbtn from './header_btn/header_btn.vue'
export default {
  components: {
    headerbtn,
  },
  data() {
    return {
      svg:require('../assets/headerlo.png'),
      traval:[
        {
          cis:'品牌旗艦館',
          rating:'旅行社評價',
          new:'最新消息',
          hotnews:'限時！註冊送500！',
        },
      ],
      login:'登入/註冊',
    }
  },
}
</script>

<style lang="sass" scoped>
  .font17
    font-size: 15px
</style>
