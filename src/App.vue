<script>
import AppHeader from './components/AppHeader.vue';
export default {
  components: {
    AppHeader
  },
  data () {
    return {
      contentNavBar: ["Home", "Missions", "Causes", "Journal", "Donate"],
    }
  }
}
</script>


<template>
  <AppHeader :navigationBar="contentNavBar"/>

</template>

<style lang="scss">
@use "./style/general.scss";
</style>