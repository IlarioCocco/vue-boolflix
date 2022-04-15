<template>
  <div id="app">
    <Header @listen="searchMovies"/>
    <Main :movies="movies" :bgImage="require('./assets/img/bkg.jpg')"/>
    <Shop/>
    <Footer/>
  </div>
</template>



<script>
import Header from './components/Header.vue';
import Main from './components/Main.vue';
import Footer from './components/Footer.vue';
import Shop from './components/Shop.vue';
import axios from 'axios';

export default {
  name: 'App',
  components: {
    Header,
    Main,
    Shop,
    Footer
  },

  data() {
    return {
      movies: [],
    }
  },

  methods: {
    searchMovies(pippo) {
      // console.log(query);
      axios.get('https://api.themoviedb.org/3/search/movie', {
       params: {
         api_key: '93138e86c1b2f8ca76e512cc0d72943b',
         query: pippo,
         language: 'it-IT',
      }
    })

    .then((response) => {
      // console.log(response.data);
      this.movies = response.data.results;
    });
    }
  }
}
</script>



<style lang="scss">
@import "./assets/scss/common.scss";
</style>
