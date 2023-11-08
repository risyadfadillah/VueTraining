<script>
export default {
    name: "MovieTitle",
    props: {
        movieTitle: {
            type: String
        },
        activeTitle: {
            type: String
        }
    },
    emits: ['onClick-Title']
}
</script>

<template>
    {{ console.log(">>>> ", activeTitle) }}
    <div class="MovieTitleContainer">
        <ul class="MovieTitleText" >
            <li @click="$emit('onClick-Title', movieTitle)" >
                {{ movieTitle }}
            </li>
        </ul>
    </div>
</template>

<style scoped>
.MovieTitleContainer {
    align-self: flex-start;
}

.MovieTitleText {
    list-style: none;
    cursor: pointer;
}
</style>