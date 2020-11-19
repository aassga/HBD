<template lang="pug">
  #app
    headerbox
    articlebox
    footerbox
</template>

<script>
import headerbox from './components/header.vue'
import articlebox from './components/content.vue'
import footerbox from './components/footer.vue'

export default {
  name: 'App',
  components: {
    headerbox,
    articlebox,
    footerbox
  },
} 
</script>
<style lang="sass" scoped>
</style>
