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
         api_key: '93138e86c1b2f8ca76e512cc0d72943b',
         query:   'Back to the Future',
         language:'en-US',
      }
    })
    .then(function (response) {
      console.log(response.data.results);
    });
  }
}
</script>




<style lang="scss">
#app {
 
  text-align: center;
  
}
</style>
