<!-- --------QUI VA I TUOI SCRIPT JS LEGATI A QUESTO COMPONENTS IN PARTICOLARE-------- -->
<script>
import AppFindUs from './AppFindUs.vue';
import AppComics from './AppComics.vue';

export default {
  name: 'AppWip',

  components:{
    AppFindUs,
    AppComics,
  },

  data(){
    return{
      
    comics :[
      {
          "thumb": "https://www.coverbrowser.com/image/action-comics/1-1.jpg",
          "price": "$19.99",
          "series": "Action Comics",
          "type": "comic book",
      },
      {
          "thumb": "https://www.panini.it/media/catalog/product/cache/a5b5dd3adfe0d321084804c738f29601/M/1/M1BLLA015ISBN_0.jpg",
          "price": "$3.99",
          "series": "American Vampire 1976",
          "type": "comic book",
      },
      {
          "thumb": "https://media.wired.com/photos/593384dad80dd005b42b2817/master/w_2560%2Cc_limit/Aquaman-16.jpg",
          "price": "$16.99",
          "series": "Aquaman",
          "type": "graphic novel",
      },
      {
          "thumb": "https://d29xot63vimef3.cloudfront.net/image/batgirl/1-1.jpg",
          "price": "$2.99",
          "series": "Batgirl",
          "type": "comic book",
      },
      {
          "thumb": "https://static.posters.cz/image/750/locandine-film-in-plexiglass-batman-prowl-comic-cover-i69653.jpg",
          "price": "$3.99",
          "series": "Batman",
          "type": "comic book",
      },
      {
          "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/5/50/Batman_Beyond_v.1_1.jpg",
          "price": "$2.99",
          "series": "Batman Beyond",
          "type": "comic book",
      },
      {
          "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/0/0d/Batman_Superman_Vol_1_1.jpg",
          "price": "$3.99",
          "series": "Batman/Superman",
          "type": "comic book",
      },
      {
          "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/c/cf/Batman_Superman_Annual_Vol_2_1.jpg",
          "price": "$4.99",
          "series": "Batman/Superman Annual",
          "type": "comic book",
      },
      {
          "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/5/54/Batman_The_Joker_War_Zone_Vol_1_1.jpg",
          "price": "$5.99",
          "series": "Batman: The Joker War Zone",
          "type": "comic book",
      },
      {
          "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/6/64/Batman_Three_Jokers_Collected.jpg",
          "price": "$6.99",
          "series": "Batman: Three Jokers",
          "type": "comic book",
      },
      {
          "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/f/f8/Batman_White_Knight_Presents_Harley_Quinn_Vol_1_1.jpg",
          "price": "$4.99",
          "series": "Batman: White Knight Presents: Harley Quinn",
          "type": "comic book",
      },
      {
          "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/c/c8/Catwoman_Vol_2_1.jpg",
          "price": "$16.99",
          "series": "Catwoman",
          "type": "graphic novel",
      },
    ]
  }}
}

</script>

<!-- --------QUI VA L'HTML-------- -->
<template>

  <div class="jumbo">
    <div class="jumbo-top"></div>
    <div class="jumbo-bottom">
      <!-- <span id="currentSeries">CURRENT SERIES</span> -->

      <div class="comic-list">

        <AppComics v-for="currentComic in comics"
        :comicImage="currentComic.thumb"
        :comicTitle="currentComic.series"
        ></AppComics>


      </div>

    </div>
  </div>

  <AppFindUs></AppFindUs>

</template>

<!-- --------QUI VA IL CSS RELATIVO A QUESTO COMPONENTE-------- -->
<style scoped lang="scss">
@use '../_variables.scss' as *;
@use '../mixin.scss' as *;

.jumbo{
  height: 1070px;
  
  
  .jumbo-top{
    background-image: url('../../public/img/jumbotron.jpg');
    background-size: cover;
    height: 400px;
  }

  .jumbo-bottom{
    #currentSeries{
      top: 370px;
      left: 140px;

      font-size: 32px;
      background-color: $primaryColor;
      padding: 8px 12px;
    }

    .comic-list{
      display: flex;
      flex-flow: row wrap;
      width: 1200px;
      height: 600px;
      margin: 20px auto;
    }
  }
}

</style>