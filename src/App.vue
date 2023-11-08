<script>
import CustomHeader from './components/atoms/CustomHeader.vue'
import MovieCatalogue from './components/organisms/MovieCatalogue.vue';
import MovieTitle from './components/organisms/MovieTitle.vue';
import data from '../src/data.json'

export default {
  components: {
    CustomHeader, MovieCatalogue, MovieTitle
  },
  data() {
    return {
      movieData: data,
      title: "",
      director: "",
      casts: "",
      genre: "",
      movieImageSrc: ""
    }
  },
  methods: {
    setCatalogue(data) {
      this.movieData.forEach((item) => {
        // console.log("kepencet >>> ", item.title);
        if (data === item.title) {

          this.title = `${item.title} (${item.year})`
          this.director = item.director
          this.casts = item.casts
          this.genre = item.genre
          this.movieImageSrc = item.poster
          console.log("kepencet >>> ", item.title);
        } 
      })
    }
  }
}
</script>

<template>
  {{ console.log("movieTitle >>> ", title)
   }}
  <CustomHeader title="Movie Catalogue"></CustomHeader>
  <div class="MainContainer">
    <MovieCatalogue :movieTitle="title" :movieImageSrc="movieImageSrc" :movieDirector="director" :movieCasts="casts" :movieGenre="genre"></MovieCatalogue>
    <div class="MovieListWrapper">
      <div v-for="item in movieData" :key="item.title" class="MovieListContainer" >
        <MovieTitle :movieTitle=item.title 
        @onClick-Title="e=> setCatalogue(e)"
        ></MovieTitle>
      </div>
    </div>
  </div>
</template>

<style scoped>
.MainContainer {
  display: flex;
  justify-content: flex-end;
  flex-direction: row;
  flex: 1;
}

.MovieListContainer {
  display: flex;
  justify-content: flex-start;
  flex-direction: row;
  padding-left: 8px;
  padding-bottom: 4px;
  padding-top: 8px;
}

.MovieListWrapper {
  flex: 1;
  background-color: whitesmoke;
}
</style>
