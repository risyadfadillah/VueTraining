<script>
export default {
    name: "MovieCatalogue",
    props: {
        movieTitle: {
            default: "Kung Fu Panda",
            type: String
        },
        movieDirector: {
            default: "",
            type: String
        },
        movieCasts: {
            default: "",
            type: String
        },
        movieGenre: {
            default: "",
            type: String
        },
        movieImageSrc: {
            type: String
        }
    }
}
</script>

<template>
    <div class="MovieCatalogueContainer">
        <div>
            <div class="ImageContainer">
                <img alt="Vue logo" class="logo" v-bind:src="movieImageSrc" width="250" height="500" />
            </div>
            <div class="DescriptionContainer">
                <p class="MovieTitle">{{ `${movieTitle}` }}</p>
                <p class="MovieDirector">{{ `Director: ${movieDirector}` }}</p>
                <p class="MovieCasts">{{ `Casts: ${movieCasts}` }}</p>
                <p class="MovieGenre">{{ `Genre: ${movieGenre}` }}</p>
            </div>
        </div>
    </div>
</template>

<style>
.MovieCatalogueContainer {
    flex-direction: column;
    display: flex;
    justify-content: flex-end;
    align-items: center;
    padding: 8pt;
    flex: 1;
}

.MovieTitle {
    font-size: large;
    font-weight: 700;
}

.DescriptionContainer {
    display: flex;
    justify-content: center;
    align-items: center;
    padding-top: 8px;
    flex-direction: column;
}

.ImageContainer {
    display: flex;
    justify-content: center;
    align-items: center;
}
</style>
