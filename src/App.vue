<script>
  import AppHeader from './components/AppHeader.vue';
  import AppBonus from './components/AppBonus.vue';

  export default {
    components:{
      AppHeader,
      AppBonus
    }
  }
</script>

<template>
  <AppHeader />
  <AppBonus />
</template>

<style lang="scss" scoped>
@use './styles/generals.scss';

</style>
