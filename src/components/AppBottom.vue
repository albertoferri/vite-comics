<!-- --------QUI VA I TUOI SCRIPT JS LEGATI A QUESTO COMPONENTS IN PARTICOLARE-------- -->
<script>

export default {
  name: 'AppBottom',
}

</script>

<!-- --------QUI VA L'HTML-------- -->
<template>

<div class="container">
    
    <section>
        <div class="links-container">
            <div class="link-left">
                <div class="link">
                    <h1>dc comics</h1>
                    <ul>
                        <li>Characters</li>
                        <li>Comics</li>
                        <li>Movies</li>
                        <li>TV</li>
                        <li>Games</li>
                        <li>Videos</li>
                        <li>News</li>
                    </ul>
                </div>
                <div class="link">
                    <h1>shop</h1>
                    <ul>
                        <li>Shop DC</li>
                        <li>Shop DC Collectibles</li>
                    </ul>
                </div>
            </div>
    
            <div class="link">
                <h1>dc</h1>
                <ul>
                    <li>Therms Of Use</li>
                    <li>Privacy policy (new)</li>
                    <li>Ad Choices</li>
                    <li>Advertising</li>
                    <li>Jobs</li>
                    <li>Subscriptions</li>
                    <li>Talent Workshops</li>
                    <li>CPSC Certificates</li>
                    <li>Ratings</li>
                    <li>Shop Help</li>
                    <li>Contact Us</li>
                </ul>
            </div>
            <div class="link">
                <h1>sites</h1>
                <ul>
                    <li>DC</li>
                    <li>MAD Magazine</li>
                    <li>DC Kids</li>
                    <li>DC Universe</li>
                    <li>DC Power Visa</li>
                </ul>
            </div>
        </div>
        <img src="/img/dc-logo-bg.png" alt=" DC logo">

    </section>
 

    

  

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

    background-image: url('/img/footer-bg.jpg');
    background-size: cover;
    height: 370px;
    
    section{
        display: flex;
        justify-content: space-between;
        width: 1200px;
        max-height: 370px;
        margin: 0 auto;

        img{
            width: 565px;
            height: auto;
            object-fit: cover;
        }
    }
    .links-container{
        @include flex-centered;
        align-items: flex-start;
        padding: 20px 0;

        .link{
            padding: 20px;

            h1{
            width: 150px;
                margin: 0;
                text-transform: uppercase;
                font-size: 22px;
            }
    
            ul{
                padding: 0;
                margin: 0;
            }
            
            li{
                list-style-type: none;
                font-size: 14px;
                opacity: .8;
            }
        }

    }


}


</style>