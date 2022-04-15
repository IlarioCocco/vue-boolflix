<template>
  <div class="cardMovies">
      <h2>{{details.title}}</h2>
      <h2>{{details.original_title}}</h2>
      <h3>{{details.original_language}}</h3>
      <h3>{{details.vote_average}}</h3>
  </div>
</template>




<script>
export default {
  name: 'Card',
  props: ['details']
}
</script>



<style  lang="scss">

 .cardMovies {
    width: calc(100% / 6 - 20px);
    margin: 10px 10px 10px 10px;
    padding: 20px;
    display: flex;
    align-items: center;
    justify-content: center;
    color: white;
    background-color: rgb(0, 0, 0);
    margin: 10px;
    font-size: 10px;
    // border: 1px solid rgb(255, 0, 0);
 }

</style>
