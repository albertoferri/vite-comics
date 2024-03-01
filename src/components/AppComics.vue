<!-- --------QUI VA I TUOI SCRIPT JS LEGATI A QUESTO COMPONENTS IN PARTICOLARE-------- -->
<script>

export default {
  name: 'AppComics',

    // questo componente per essere visualizzato correttamente
    // esige alcune proprietà (props)
    props: {
        // dobbiamo dare un nome a queste proprietà
        // per ognuna di esse dobbiamo indicare nome e TIPO DI DATO
        // String, Number, Boolean, Array, Object
        comicTitle: String,
        comicImage: String
    },

}
</script>

<!-- --------QUI VA L'HTML-------- -->
<template>

    <div class="comic"> 
        <img :src="comicImage" :alt="comicTitle">
        <h4>{{ comicTitle }}</h4>
    </div>

  

</template>

<!-- --------QUI VA IL CSS RELATIVO A QUESTO COMPONENTE-------- -->
<style scoped lang="scss">

.comic {
    width: calc(100% / 6);
    height: 350px;
    padding: 20px;

    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 10px;
    
    img {
        width: 100%;
    }

    h4{
        text-align: center;
    }


}


</style>