<template>
  <div class="containerMovies">
<!-- utilizzo dei componeni -->
      <Card/>
   
  </div>
</template>



<script>
// importazione dei componenti
//+
//registrazione dei componenti
import Card from './Card.vue';
export default {
  name: 'Movies',
  components: {
      Card
  }
 
}
</script>







<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

</style>
