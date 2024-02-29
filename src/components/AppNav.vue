<!-- --------QUI VA I TUOI SCRIPT JS LEGATI A QUESTO COMPONENTS IN PARTICOLARE-------- -->
<script>
export default {
  name: 'AppNav',
  data() {
        return {
            links: [
              'characters',
              'comics',
              'movies',
              'tv',
              'games',
              'collectibles',
              'videos',
              'fans',
              'news',
              'shop',
            ]
        }
    }
}

</script>

<!-- --------QUI VA L'HTML-------- -->
<template>
  <div class="container">
    <nav>
        <img src="/img/dc-logo.png" alt=" DC logo">
        <ul>
          <li v-for="(link, index) in links" :key="index">
            {{ link }}
          </li>
        </ul>

    </nav>
  </div>
</template>

<style scoped lang="scss">
// VARIABILI CSS
@use '../_variables.scss' as *;
@use '../mixin.scss' as *;

.container{
  background-color: white;

  nav{
    @include flex-centered;
    justify-content: space-between;

    width: 1200px;
    height: 120px;
    margin: 0 auto;

    img{
      height: 80px;
      width: auto;
      cursor: pointer;
    }

    ul{
      display: flex;
      padding: 0;
      margin: 0;

      li{
        list-style-type: none;
        font-weight: bold;
        text-transform: uppercase;
        font-size: 12px;
        cursor: pointer;
        color: black;
        min-height: 120px;
        @include flex-centered;
        border-bottom: 3px transparent solid;
        padding: 0 10px;

        
  
        &:hover{
          color: $primaryColor;
          border-color: $primaryColor;
          transition: .2s ease-in-out;
        }
        &:not(:hover){
          color: black;
          border-color: transparent;
          transition: .2s ease-in-out;
        }
      }

    }


  }

}




</style>