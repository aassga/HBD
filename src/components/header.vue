<template lang="pug">
  header
    section#header
      .container
        .row
          .col-12
            .row
              .col-sm-5
                img(:src="svg")
              .col-sm-7
                b-nav.font17
                  b-nav-item 品牌旗艦館
                  b-nav-item 旅行社評價
                  b-nav-item 最新消息 
                    span.text-warning 限時！註冊送500！
                  b-nav-item 
                    button.btn.btn-sm.btn-info(type='button') 登入/註冊
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
    }
  },
}
</script>

<style lang="sass" scoped>
  .font17
    font-size: 15px
</style>
