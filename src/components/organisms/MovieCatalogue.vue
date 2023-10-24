<script>
export default {
    name: "MovieCatalogue",
    props: {
        title: {
            default: "Kung Fu Panda",
            type: String
        }
    }


}
</script>

<template>
    <img alt="Vue logo" class="logo" src="../../assets/logo.svg" width="125" height="125" />
    <p class="MovieTitle">{{ `${title} ${"(2008)"}` }}</p>
    <p class="MovieDirector">{{ `Director: ${director}` }}</p>
    <p class="MovieCasts">{{ `Casts: ${casts}` }}</p>
    <p class="MovieGenre">{{ `Genre: ${genre}` }}</p>
</template>

<style>
/* .MovieTitle {
    
} */

</style>