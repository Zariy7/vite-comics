<script>
  import AppHeader from './components/AppHeader.vue';
  import AppBonus from './components/AppBonus.vue';
  import AppFooter from './components/AppFooter.vue';
  import AppMain from './components/AppMain.vue';

  export default {
    components:{
      AppHeader,
      AppBonus,
      AppFooter,
      AppMain
    }
  }
</script>

<template>
  <AppHeader />
  <AppMain />
  <AppBonus />
  <AppFooter />
</template>

<style lang="scss" scoped>
@use './styles/generals.scss';

</style>
