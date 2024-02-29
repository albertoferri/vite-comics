<!-- --------QUI VA I TUOI SCRIPT JS LEGATI A QUESTO COMPONENTS IN PARTICOLARE-------- -->
<script>
export default {
  name: 'AppNav',
}

</script>

<!-- --------QUI VA L'HTML-------- -->
<template>
  <div class="container">
    <nav>
        <img src="/img/dc-logo.png" alt=" DC logo">
        <ul>
          <li>characters</li>
          <li>comics</li>
          <li>movies</li>
          <li>tv</li>
          <li>games</li>
          <li>collectibles</li>
          <li>videos</li>
          <li>fans</li>
          <li>news</li>
          <li>shop</li>
        </ul>
    </nav>
  </div>
</template>

<style lang="scss">

.container{
  background-color: white;

  nav{
    display: flex;
    align-items: center;
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
    }

  }

}




</style>