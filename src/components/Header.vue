<template>
  <div class="header">
      <!-- searchMovies è methods
      <input type="text" v-model="searchMovies" placeholder="search Movies">
      <button @click="$emit('listen', searchMovies)">Search</button> -->
    <form>
      <input type="text" v-model="searchMovies" placeholder="search Movies">
      <button type="submit" @click.prevent="$emit('listen', searchMovies)">Search</button>
    </form>
  </div>
</template>



<script>

export default {
  name: 'Header',
  data() {
      return {
        searchMovies: ""
      }
  }
 
}
</script>







<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

</style>
