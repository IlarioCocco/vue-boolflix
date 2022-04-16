<template>
    <main :style="`background-image: url(${bgImage})`">
        <div class="boxMainShadow">
            <div class="titolo">
              <h2>Film, serie TV e tanto altro. <br> Senza limiti. </h2>
              <h6 class="guarda">Guarda ciò che vuoi ovunque. Disdici quando vuoi.</h6>
            </div>
          
            <div class="boxDue">
              <MovieCard v-for="(todo, i) in arrayMovies" :key="i" 
              :info="todo"/>
            </div>
        </div>
    </main>
</template>




<script>
import MovieCard from './MovieCard.vue';
export default {
  name: 'Movies',
  props: ['arrayMovies','bgImage'],
  

  components: {
    MovieCard
  }
}
</script>




<style  lang="scss">
.boxMainShadow {
  max-width: 100%;
  max-height: 100%;
  margin: auto;
  padding: 100px;
  background: linear-gradient(#000000, #00000043, #000000);
  height: 100vh;
  color: white;
  // border: 5px solid greenyellow;
}

main {
  // padding: 200px 30px 30px 30px;
  max-width: 100%;
  margin:auto;
  background-position: top;
  background-size: cover;
  background-repeat: no-repeat;
  height: 100vh;
  filter: brightness(100%);
  // border: 5px solid rgb(255, 183, 0);
}

.boxDue {
  max-width: 90%;
  margin: auto;
  flex-wrap: wrap;
  display: flex;
  background: linear-gradient(#ffffff00, #76000000, #ff000000);
  margin-top: 20px;
  margin-bottom: 50px;
  height: 50vh;
  overflow: auto;
  // border: 5px solid rgb(255, 0, 0);
  // border: 20px solid rgb(0, 0, 0);

}

::-webkit-scrollbar{
  width:0.8em;
  height:0.8em;
  background: #ff00003d;
  margin-right: 10px;
}
::-webkit-scrollbar:hover{
  background-color:#ff0000 ;
  border: none;
  display: block;
}


.titolo {
  max-width: 90%;
  margin: auto;
  display: inline-flexbox;
  justify-content: center;
  margin-top: 65px;
  // text-transform: uppercase;
  font-size: 40px;
  text-align: center;
  // border: 5px solid rgb(255, 0, 128);
}

.guarda {
 padding-top: 20px;
 font-weight: 100;
}

</style>
