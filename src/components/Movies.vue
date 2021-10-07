<template>
  <div class="containerMovies">
<!-- utilizzo dei componeni -->
    <ul class="cardList">
        <li v-for="(movie, index) in movies" :key="index">
            <Card details="movie"/>
        </li>
    </ul>
  </div>
</template>



<script>
// importazione dei componenti
import Card from './Card.vue';

// registrazione dei componenti
export default {
  name: 'Movies',
// il nome della props di Movies.vue deve dialogare 
// con la props di App.vue :movies presente in App.vue genitore
  props: ['movies'],

  components: {
      Card
  }
 
}
</script>




<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

.cardList {
    // list-style: none;
}

</style>
