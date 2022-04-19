<template>
  <div id="app">
    <Header @listen="searchMovies"/>
    <Movies :arrayMovies="arrayMov" 
            :arraySeries="arrayTv"
    :bgImage="require('./assets/img/bkg.jpg')"/>
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
      arrayMov: [],
      arrayTv: []
    }
  },

  methods: {
    searchMovies(richiesta) {
      const params = {
        api_key: 'e99307154c6dfb0b4750f6603256716d',
        query: richiesta,
        language: 'it-IT',

      }
      // console.log(query);
//-----------------call movies
      axios.get('https://api.themoviedb.org/3/search/movie', {
        params: params
    })
    .then((response) => {
      console.log(response.data);
      this.arrayMov = response.data.results;
    });


//---------------call serie tv  
      axios.get('https://api.themoviedb.org/3/search/tv', {
        params: params
    })
    .then((response) => {
      console.log(response.data);
      this.arrayTv = response.data.results;
    });

    }
  }
}
</script>


<style lang="scss">
@import "./assets/scss/common.scss";
</style>
