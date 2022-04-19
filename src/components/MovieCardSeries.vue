<template>
  <div class="cardMovies">
      <img class="img" :src="`https://image.tmdb.org/t/p/w300${info.poster_path}`">
      <h2 class="title">{{info.name}}</h2>
      <h2 class="titleOriginal">{{info.original_name}}</h2>
      <h3 class="language">language:
        <lang-flag class="flag" :iso="info.original_language" :squared="false"/>
      </h3>
      <h3 class="vote"><span class="colorVote">vote:</span> {{info.vote_average}}</h3>
  </div>
</template>




<script>
import LangFlag from 'vue-lang-code-flags';
export default {
  name: 'MovieCardSeries',
  props: ['info'],
  components: {
    LangFlag,
  }
}
</script>



<style scoped lang="scss">

 .cardMovies {
    width: calc(100% / 6 - 20px);
    margin: 10px 10px 10px 10px;
    padding: 10px;
    display: flex;
    flex-wrap: wrap;
    align-items: center;
    justify-content: center;
    color: white;
    background-color: rgba(156, 36, 36, 0.525);
    margin: 10px;
    font-size: 10px;
    border: 1px solid rgba(255, 255, 255, 0.208);
    border-radius: 5px;
 }

 .img {
    width: 100%;
    padding: 0px 0px 0px 0px; 
    cursor: pointer;
    // position: relative;
    border: 3px solid rgba(255, 255, 255, 0);
    clip-path: inset(0% 0% 0% 0%);
    filter: brightness(80%);

    &.img:hover {
        filter: brightness(100%);
        border: 3px solid rgb(255, 255, 255);
    }
}
.title {
  font-size: 20px;
  padding: 15px 15px 0px 15px;
  max-width: 100%;
  text-align: center;
}
.titleOriginal {
  font-size: 15px;
  padding: 10px 15px 0px 15px;
  color: rgb(250, 175, 0);
  width: 100%;
  text-align: center;
}

.language {
  margin-right: 5px;
  padding: 10px 15px 10px 15px;
  display: flex;
  align-items: center;
}

.vote {
  color: rgb(219, 168, 0);
  padding: 10px 15px 10px 15px;
  font-weight: bold;
  .colorVote {
    color: rgb(255, 0, 0);
  }
}

.flag {
  padding-left: 40px;
  font-size: 20px;
}

</style>
