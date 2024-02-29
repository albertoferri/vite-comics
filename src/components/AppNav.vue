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
$primaryColor: #0282f9;


@mixin flex-centered{
    display: flex;
    justify-content: center;
    align-items: center;
}

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
      gap: 30px;
      padding: 0;
    }

    li{
      list-style-type: none;
      font-weight: bold;
      text-transform: uppercase;
      font-size: 12px;
      cursor: pointer;
      color: black;
    }

  }

}




</style>