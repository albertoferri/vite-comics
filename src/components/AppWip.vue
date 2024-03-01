<!-- --------QUI VA I TUOI SCRIPT JS LEGATI A QUESTO COMPONENTS IN PARTICOLARE-------- -->
<script>
import AppFindUs from './AppFindUs.vue';

export default {
  name: 'AppWip',
  components:{
    AppFindUs,
  }
}

</script>

<!-- --------QUI VA L'HTML-------- -->
<template>

  <div class="container">
    <div class="wip">
      ---- WORK IN PROGRESS ----

    </div>



  </div>
  <AppFindUs></AppFindUs>

</template>

<!-- --------QUI VA IL CSS RELATIVO A QUESTO COMPONENTE-------- -->
<style scoped lang="scss">


.container{
  display: flex;
  align-items: center;
  height: 130px;
  .wip{
    margin: 0 auto;
    width: 1200px;
    font-size: 30px;
    font-weight: bold;
  }
  
}

</style>