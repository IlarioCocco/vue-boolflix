<template>
  <div id="app">
    <Header/>
    <Movies/>
  </div>
</template>



<script>
import Header from './components/Header.vue';
import Movies from './components/Movies.vue';
// import axios from '.axios'

export default {
  name: 'App',
  components: {
    Header,
    Movies
  },

}
</script>




<style lang="scss">
#app {
 
  text-align: center;
  
}
</style>
