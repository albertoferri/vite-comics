<!-- --------QUI VA I TUOI SCRIPT JS LEGATI A QUESTO COMPONENTS IN PARTICOLARE-------- -->
<script>

export default {
  name: 'AppFooter',
}

</script>

<!-- --------QUI VA L'HTML-------- -->
<template>

<div class="container">
  <footer>
    <button>Sign-up now!</button>
    <ul class="social">
      <li>FOLLOW US</li>
      <li><img src="/img/footer-facebook.png" alt=""></li>
      <li><img src="/img/footer-twitter.png" alt=""></li>
      <li><img src="/img/footer-youtube.png" alt=""></li>
      <li><img src="/img/footer-pinterest.png" alt=""></li>
      <li><img src="/img/footer-periscope.png" alt=""></li>
    </ul>
  </footer>

  

</div>




</template>

<style scoped lang="scss">
// VARIABILI CSS
@use '../_variables.scss' as *;
@use '../mixin.scss' as *;

.container{
  background-color: #303030;
  height: 110px;
  
  footer{
    @include flex-centered;
    justify-content: space-between;  
    width: 1200px;
    height: 100%;
    margin: 0 auto;

    button{
      text-transform: uppercase;
      padding: 10px 14px;
      border: none;
      background-color: white;
      color: black;
      font-weight: bold;
      border-radius: 8px;
      cursor: pointer;

      &:hover{
        background-color: $primaryColor;
        transition: .3s ease-in-out;
      }

      &:not(:hover){
        background-color: white;
        transition: .3s ease-in-out;
      }
    }
    .social{
      @include flex-centered;
      gap: 20px;
      padding: 0;

      li{
        list-style-type: none;
        cursor: pointer;

        &:hover{
          filter: invert(1);
        }
      }

      li:first-child{
        color: $primaryColor;
        font-weight: bold;
      }
    }
  }

}


</style>