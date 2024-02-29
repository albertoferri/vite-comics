<!-- --------QUI VA I TUOI SCRIPT JS LEGATI A QUESTO COMPONENTS IN PARTICOLARE-------- -->
<script>

export default {
  name: 'AppBottom',
  data() {
    return {
        links: [
            {
                titolo: 'dc comics',
                items: [
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
            },
            {
                titolo: 'shop',
                items: [
                    'Shop DC',
                    'Shop DC Collectibles',
                ]
            },
            {
                titolo: 'dc',
                items: [
                    'Therms Of Use',
                    'Privacy policy (new)',
                    'Ad Choices',
                    'Advertising',
                    'Jobs',
                    'Subscriptions',
                    'Talent Workshops',
                    'CPSC Certificates',
                    'Ratings',
                    'Shop Help',
                    'Contact Us',
                ]
            },
            {
                titolo: 'sites',
                items: [
                    'DC',
                    'MAD Magazine',
                    'DC Kids',
                    'DC Universe',
                    'DC Power Visa',
                ]
            },
        ]
    }
}

}

</script>

<!-- --------QUI VA L'HTML-------- -->
<template>

<div class="container">
    
    <section>
        <div class="links-container">
            <div class="link" v-for="link in links" :key="link.titolo">
                <h1>{{ link.titolo }}</h1>
                <ul>
                    <li v-for="item in link.items" :key="item">{{ item }}</li>
                </ul>
            </div>
        </div>


        <img src="/img/dc-logo-bg.png" alt=" DC logo">

    </section>

</div>




</template>

<style scoped lang="scss">
// VARIABILI CSS
@use '../_variables.scss' as *;
@use '../mixin.scss' as *;

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
                cursor: pointer;
            }
    
            ul{
                padding: 0;
                margin: 0;
            }
            
            li{
                list-style-type: none;
                font-size: 14px;
                opacity: .8;
                cursor: pointer;
            }

            li:hover{
                opacity: 1;
            }

        }

    }


}


</style>