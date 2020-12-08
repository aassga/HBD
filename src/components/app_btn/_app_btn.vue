<template lang="pug">
  div
    button.mb-xl-0.mr-2.mr-lg-2(:class="appObject" @click="msg")
      span.d-flex.align-items-center
        span.icon.mr-2
          span.text-info.fab.fa-apple
        span.d-inline-block
          small(:class="smalltext") {{ Available }}
          | {{ appstore }}
    button(:class="appObject" @click="msg")
      span.icon.mr-2
        span.text-info.fab.fa-google-play
      span.d-inline-block
        small(:class="smalltext") {{ Available }}
        | {{ googleplay }}
</template>
<script>
export default {
  data() {
    return {
      appObject: {
        'btn': true,
        'btn-light': true,
        'ft600': true,
      },
      smalltext:{
        'd-block': true,
        'font-weight-bold': true,
      },
      Available:"適用於",
      appstore:"App Store",
      googleplay:"Google Play",
    }
  },
  methods: {
    msg(){
      alert('敬請期待上線')
    }
  },
}
</script>

<style lang="sass" scoped>
  .ft600
    font-weight: 600
</style>
