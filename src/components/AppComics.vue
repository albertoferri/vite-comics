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
@use '../_variables.scss' as *;
@use '../mixin.scss' as *;

.comic {
    width: calc(100% / 6);
    height: 300px;
    padding: 20px;

    display: flex;
    flex-direction: column;
    cursor: pointer;

    transition: box-shadow 0.3s ease-in-out;

    &:hover{
        box-shadow: 0 0 20px rgba(255, 255, 255, 0.1);
    }
    
    img {
        width: 100%;
        height: 186px;
        object-fit: cover;
        object-position: top;
    }

    h4{
        text-transform: uppercase;
        padding: 10px 0;
    }


}


</style>