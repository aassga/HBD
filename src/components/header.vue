<template lang="pug">
  header
    section.border-bottom.mt-4.pb-4
      .container
        .row
          .col-12
            //logo區域
            headerlogo
    section.mb-4.shadow-sm.rounded
      .container
        .row
          .col-12
            //btn按鈕區域
            headerbtn
        

</template>
<script>
import headerlogo from './header_btn/_header_logo.vue'
import headerbtn from './header_btn/_header_btn.vue'
export default {
  components: {
    headerlogo,
    headerbtn,
  },
}
</script>

<style lang="sass" scoped>
  .font17
    font-size: 15px
</style>
