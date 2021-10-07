<template>
  <div id="app">
    <Header/>
    <Movies/>
  </div>
</template>



<script>
import Header from './components/Header.vue';
import Movies from './components/Movies.vue';
import axios from 'axios';

export default {
  name: 'App',
  components: {
    Header,
    Movies
  },

  created(){
    axios.get('https://api.themoviedb.org/3/search/movie', {
       params: {
         api_key: 'e99307154c6dfb0b4750f6603256716d',
         query: 'ritorno+al+futuro',
         language: 'it-IT',
      }
    })
    .then(function(risposta) {
      console.log(risposta.data);
    });
  }
}
</script>




<style lang="scss">
#app {
 
  text-align: center;
  
}
</style>
