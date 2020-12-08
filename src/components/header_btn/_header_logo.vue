<template lang="pug">
  .row.justify-content-center.align-items-center
    .col-sm-2
      img(:src="svg" alt='logo')
    .col-sm-3
      .gov3000_icon
        a(href='#')
          img(:src="icon_svg" alt='icon')  
    .col-sm-7.row.justify-content-end
      b-nav.font17(v-for="(item,i) in traval" :key="item.traval")
        b-nav-item(:class="fontObject") {{ item.cis }}
        b-nav-item(:class="fontObject") {{ item.rating }}
        b-nav-item(:class="fontObject") {{ item.new }}
          span.text-warning.pl-2 {{ item.hotnews }}
        b-nav-item 
          button.btn.btn-sm.btn-info(type='button') {{ login }}

</template>
<script>
export default {
  data() {
    return {
      svg:require('../../assets/headerlo.png'),
      icon_svg:'https://dszfbyatv8d2t.cloudfront.net/img/icon_gov3000.png',
      traval:[
        {
          cis:'品牌旗艦館',
          rating:'旅行社評價',
          new:'最新消息',
          hotnews:'限時！註冊送500！',
        },
      ],
      login:'登入/註冊',
      fontObject:{
        'mt-1': true, 
        'font-weight-bold': true,
      },
    }
  },
}
</script>

<style lang="sass" scoped>
  .font17
    font-size: 15px
  .gov3000_icon 
    width: 60px
    margin-left: 20px
    opacity: .8  
    img 
      width: 100%
</style>
