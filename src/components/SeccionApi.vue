<template>
  <div id ="noticias">
    <div class="row mt-md-5 mt-sm-5 mt-xs-5">
      <div
        class="col-lg-6 col-xs-12"
        v-for="(movie, index) of movies"
        :key="index"
      >
        <div class="d-flex justify-content-center align-items-center">
          <div class="p-3">
            <img :src="movie.Poster" alt="Imagen de la Pelicula" />
          </div>
          <div>
            <h3>{{ movie.Title }}</h3>
            <hr />
          </div>

          <div class="p-2">
            <p>
              Harry Potter es una serie de novelas fantásticas escrita por la
              autora británica J. K. Rowling, en la que se describen las
              aventuras del joven aprendiz de magia y hechicería Harry Potter y
              sus amigos Hermione Granger y Ron Weasley, durante los años que
              pasan en el Colegio Hogwarts de Magia y Hechicería.
            </p>
          </div>
        </div>
        <div class="d-flex container-fluid justify-content-end mt-n5">
          <a
            class="btn btn-outline-info"
            :href="'https://www.imdb.com/title/' + movie.imdbID"
            target="_blank"
            rel="nooper noreferrer"
            >Ver</a
          >
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import axios from "axios";
export default {
  name: "SeccionApi",
  data() {
    return {
      movies: null,
    };
  },
  mounted() {
    axios
      .get("http://www.omdbapi.com/?s=harry+potter&type=movie&apikey=bd618f29")
      .then((response) => {
        this.movies = response.data.Search.slice(0, 4);
        console.log(this.movies);
      });
  },
};
</script>

<style scoped></style>
