<!-- --------QUI VA I TUOI SCRIPT JS LEGATI A QUESTO COMPONENTS IN PARTICOLARE-------- -->
<script>
export default {
  name: 'AppFindUs',
}

</script>

<!-- --------QUI VA L'HTML-------- -->
<template>

<div class="container">
    <ul id="libraries">
        <li>
            <img src="/img/buy-comics-digital-comics.png" alt="">
            <span>Digital comics</span>
        </li>
        <li>
            <img src="/img/buy-comics-merchandise.png" alt="">
            <span>dc merchandise</span>
        </li>
        <li>
            <img src="/img/buy-comics-subscriptions.png" alt="">
            <span>subscription</span>
        </li>
        <li>
            <img src="/img/buy-comics-shop-locator.png" alt="">
            <span>comic shop locator</span>
        </li>
        <li>
            <img src="/img/buy-dc-power-visa.svg" alt="">
            <span>dc power visa</span>
        </li>
    </ul>
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
    height: 155px;
    background-color: $primaryColor;
    @include flex-centered;
    
    #libraries{
        width: 1200px;
        margin: 0 auto;

        display: flex;
        justify-content: space-between;
        padding: 0;
    }

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
        }
    }
}

</style>