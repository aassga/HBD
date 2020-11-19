<template lang="pug">
  footer.footer.pb-5.bg-primary.text-white.pt-9.mt-n9
    .container
      .row.mt-6
        .col-xl-3.mb-3.mb-xl-0
          img.mb-3(src='../assets/treelogo.png' height='' alt='treelogo')
          span.small.text-secondary {{ wellcome }}
        .col-6.col-xl-2.mb-5.mb-xl-0
          span(v-text="themesberg" :class="hlistObject")
          ul(:class="flinkObject")
            li.small(v-for="(item,i) in traval" :key="i.traval")
              a(target='_blank' href='#') {{ item.name }}

        .col-6.col-xl-3.mb-5.mb-xl-0
          span(v-text="other" :class="hlistObject")
          ul(:class="flinkObject")
            li.small(v-for="(item,i) in features" :key="i.features")
              a(href='#') {{ item.name }}
              
        .col-12.col-xl-4.mb-5.mb-xl-0
          p 下載 HTD App

          //app download
          appbtn

      hr.my-3.my-lg-4
      .row
        .col.mb-md-0
          div(:class="footerObject")
            span.mb-3.fas.fa-angle-double-down
          div(:class="footerObject")
            p.font-weight-normal.small.mb-0 {{ Copyright }} 

</template>
<script>
import appbtn from './app_btn/app_btn.vue'
export default {
  components:{
    appbtn,
  },
  data() {
    return {
      wellcome:"歡迎來到 HTD 嘎嘎旅遊去 ----- Happy Traval Date 請盡情瀏覽",
      themesberg:"認識嘎嘎旅遊",
      other:"旅客服務",
      Copyright:"Copyright © 2020 HTD . All rights reserved.",
      traval:[
        { name:'關於我們' },
        { name:'官方部落格' },
        { name:'服務條款' },
        { name:'隱私權政策' },
        { name:'免責聲明' },
        { name:'公司公告' },
      ],
      features:[
        { name:'熱門打卡景點' },
        { name:'推薦行程' },
        { name:'' },
        { name:'' },
      ],
      hlistObject:{
        'h6': true, 
        'font-weight-light': true,
      },
      flinkObject:{
        'footer-links': true, 
        'mt-2': true, 
      },
      footerObject: {
        'd-flex': true,
        'justify-content-center': true,
      },
    }
  },
}
</script>
<style lang="sass" scoped>
  .bg-primary 
    background-color: #012240!important
  .footer 
    ul 
      margin-bottom: 0
      padding: 0
      list-style: none
      li
        a
          text-decoration: none
          position: relative
          display: block
    .footer-links 
      li 
        display: block
        margin-left: -5px
        margin-right: -5px
        a
          padding: 5px
          color:#8e8e8e
          &:hover 
            color: #c33c54
            transition: 0.8s
</style>
