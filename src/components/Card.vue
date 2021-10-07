<template>
  <div class="cardMovies">
      <h2>{{details.title}}</h2>
      <h4>{{details.original_title}}</h4>
      <div>{{details.original_language}}</div>
      <div>{{details.vote_average}}</div>
  </div>
</template>




<script>
export default {
  name: 'Card',
  props: ['details']
}
</script>




<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
    

</style>
