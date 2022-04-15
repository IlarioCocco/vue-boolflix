<template>
    <main :style="`background-image: url(${bgImage})`">
      <div class="boxMainShadow">
        <div class="titolo">
          <h2>Film, serie TV e tanto altro. <br> Senza limiti. </h2>
          <h6>Guarda ciò che vuoi ovunque. Disdici quando vuoi.</h6>
        </div>
        
          <div class="boxDue">
            <Card v-for="(movie, i) in movies" :key="i" :details="movie"/>
          </div>
      </div>
    </main>
</template>



<script>
import Card from './Card.vue';
export default {
  name: 'Movies',
  props: ['movies', 'bgImage' ],
  

  components: {
      Card
  }
}
</script>




<style  lang="scss">
.boxMainShadow {
  max-width: 100%;
  max-height: 100%;
  margin: auto;
  padding: 100px;
  background: linear-gradient(#000000, #0000006f, #000000);
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
  background: radial-gradient(#ffffff2d, #ffffff00, #ff000000);
  margin-top: 20px;
  margin-bottom: 50px;
  // border: 5px solid rgb(255, 0, 0);
  height: 50vh;
  overflow: auto;
  // border: 20px solid rgb(0, 0, 0);

}

::-webkit-scrollbar{
  width:0.8em;
  height:0.8em;
  background: #ff0000;
  margin-right: 10px;
}

.titolo {
  max-width: 90%;
  margin: auto;
  display: inline-flexbox;
  justify-content: center;
  margin-top: 65px;
  // text-transform: uppercase;
  font-size: 30px;
  text-align: center;
  // border: 5px solid rgb(255, 0, 128);
}

</style>
