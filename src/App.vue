<script>
  import AppHeader from './components/AppHeader.vue';
  import AppBonus from './components/AppBonus.vue';
  import AppFooter from './components/AppFooter.vue';


  export default {
    components:{
      AppHeader,
      AppBonus,
      AppFooter
    }
  }
</script>

<template>
  <AppHeader />
  <AppBonus />
  <AppFooter />
</template>

<style lang="scss" scoped>
@use './styles/generals.scss';

</style>
