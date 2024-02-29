<!-- --------QUI VA I TUOI SCRIPT JS LEGATI A QUESTO COMPONENTS IN PARTICOLARE-------- -->
<script>
export default {
  name: 'AppFindUs',
  data() {
  return {
    items: [
      { img: '/img/buy-comics-digital-comics.png', label: 'Digital comics' },
      { img: '/img/buy-comics-merchandise.png', label: 'DC merchandise' },
      { img: '/img/buy-comics-subscriptions.png', label: 'Subscription' },
      { img: '/img/buy-comics-shop-locator.png', label: 'Comic shop locator' },
      { img: '/img/buy-dc-power-visa.svg', label: 'DC power visa' }
    ]
   }
  }

}

</script>

<!-- --------QUI VA L'HTML-------- -->
<template>

<div class="container">
    <ul id="libraries">
  <li v-for="(item, index) in items" :key="index">
    <img :src="item.img" :alt="item.label">
    <span>{{ item.label }}</span>
  </li>
</ul>

</div>

</template>

<style scoped lang="scss">
@use '../_variables.scss' as *;
@use '../mixin.scss' as *;



.container{
    height: 155px;
    background-color: $primaryColor;
    @include flex-centered;
    
    #libraries{
        width: 1200px;
        margin: 0 auto;

        display: flex;
        justify-content: space-between;
        padding: 0;

        li{
            list-style-type: none;
            text-transform: uppercase;
            display: flex;
            cursor: pointer;
            
    
            img{
                max-width: 55px;
                width: auto;
                height: 55px;
                vertical-align: middle;
            }
    
            span{
                display: flex;
                align-items: center;
                width: 160px;
                margin-left: 10px;
                font-size: 14px;
                font-weight: bold;

                &:hover{
                    text-decoration: underline;
                }
            }
        }
    }

}

</style>