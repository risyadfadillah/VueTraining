<script>
export default {
    name: "MovieList",
    props: {
        movieList: {
            default: ["Kung Fu Panda 1","Kung Fu Panda 2", "Kung Fu Panda 3"],
            type: Array
        }
    }


}
</script>

<template>
    <p v-for="(item, index) in movieList" :key="item.index">
        {{ item }}
    </p>
</template>

<style>
/* .MovieTitle {
    
} */

</style>