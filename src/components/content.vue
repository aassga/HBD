<template>
  <div>
    123
  </div>
</template>
<script>
import axios from "axios" 
export default {
  data() {
    return {
      searchKey:{
        idspreadId: '1qYprnANhi5Lmr9ejz55Ae3D662yGOP66zwoTkMkhlok',
        sheetId : '133963212',
        disableCache: '1',
      }
    }
  },
  mounted() {
    this.getMenuList()
  },
  methods: {
    getMenuList(){
      const url = `https://www.tripresso.com/api_v2/google_sheet/ajaxGetSheet/?idspread_sheet_id=${this.searchKey.idspreadId}&sheet_id=${this.searchKey.sheetId}&disable_cache=${this.searchKey.disableCache}`;
      axios.get(url)
        .then(() => {

        })
        .catch(() => {

        });
    }
  },
}
</script>

<style lang="sass" scoped>
</style>
