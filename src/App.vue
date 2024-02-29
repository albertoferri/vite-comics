<script>
import AppNav from './components/AppNav.vue';
import AppWip from './components/AppWip.vue';
import AppFindUs from './components/AppFindUs.vue';
import AppFooter from './components/AppFooter.vue';
import AppBottom from './components/AppBottom.vue';

export default{
  components:{
    AppNav,
    AppWip,
    AppFindUs,
    AppBottom,
    AppFooter,
  }
}

</script>

<template>

  <AppNav></AppNav>
  <AppWip></AppWip>
  <AppFindUs></AppFindUs>
  <AppBottom></AppBottom>
  <AppFooter></AppFooter>

</template>

<style>

</style>
