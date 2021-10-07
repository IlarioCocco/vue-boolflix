<template>
  <div id="app">
    <!-- tramite la @ e l'arogmento ("listen") parso dei dati da componente figlio a genitore.
    il componente figlio ovvero Header.vue deve Emettere($emit) un evento!
    ("listen") ovvero il primo parametro puo essere chiamato come vogliamo,
    il secondo parametro (searchMovies) invece è un valore.
    in questo caso si passa un valore ("listen") = al campo della input (searchMovies)
    cosichè il nostro genitore App.Vue possa rimanere in ascolto con il @listen che deve matchare(mecciare)
    con il nome dell'evento ovvero (searchMovies) in modo da richiamre un metodo quando 
    voene richiamato -->
    <Header @listen="searchMovies"/>
    <Movies :movies="movies"/>
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

  // created(){
  //   axios.get('https://api.themoviedb.org/3/search/movie', {
  //      params: {
  //        api_key: '93138e86c1b2f8ca76e512cc0d72943b',
  //        query:   'Back to the Future',
  //        language:'en-US',
  //     }
  //   })
  //   .then(function (response) {
  //     console.log(response.data.results);
  //   });
  // },


  // data
  // inizialmente mi creerò una variabile in data di nome movies che inizialmente 
  // sarà un array vuoto, poi tramite la PROPS passerò i film
  data() {
    return {
      movies: [],
    }
  },

  methods: {
    // pippo è un argomento che viene utilizzato da vue.js in automatico,
    // vue.js dice: nel metodo del genitore aggiungi un parametro,
    // vue.js andrà poi a parsare i dati di input dentro al parametro
    // o argomento di methods ovvero pippo 
    searchMovies(pippo) {
      // console.log(query);
      axios.get('https://api.themoviedb.org/3/search/movie', {
       params: {
         api_key: '93138e86c1b2f8ca76e512cc0d72943b',
         //al posto del titolo specifico inserisco pippo
         query: pippo,
         language: 'it-IT',
      }
    })
// utilizzare sempre arrow function in funzione di callback
// cosi da lavorare dentro vue.js
    .then((response) => {
      // console.log(response.data);
      this.movies = response.data.results;
    });
    }
  }
}
</script>








<style lang="scss">
 

</style>
