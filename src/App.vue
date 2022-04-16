<template>
  <div id="app">
    <Header @listen="searchMovies"/>
    <Movies :arrayMovies="array" :bgImage="require('./assets/img/bkg.jpg')"/>
    <Shop/>
    <Footer/>
  </div>
</template>


<script>
import Header from './components/Header.vue';
import Movies from './components/Movies.vue';
import Footer from './components/Footer.vue';
import Shop from './components/Shop.vue';
import axios from 'axios';

export default {
  name: 'App',
  components: {
    Header,
    Movies,
    Shop,
    Footer
  },

  data() {
    return {
      array: [],
    }
  },

  methods: {
    searchMovies(richiesta) {
      // console.log(query);
      axios.get('https://api.themoviedb.org/3/search/movie', {
       params: {
         api_key: '93138e86c1b2f8ca76e512cc0d72943b',
         query: richiesta,
         language: 'it-IT',
      }
    })

    .then((response) => {
      console.log(response.data);
      this.array = response.data.results;
    });
    }
  }
}
</script>


<style lang="scss">
@import "./assets/scss/common.scss";
</style>
