<script>
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
export default {
  components: {
    AppHeader,
    AppMain
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
  <AppMain />

</template>

<style lang="scss">
@use "./style/general.scss";
</style>