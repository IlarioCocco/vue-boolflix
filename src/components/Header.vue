<template>
    <header>
      <div class="boxUno">
        <div>
          <img class="logoNetflix" src="../assets/img/netflixLogoTipo.png" alt="logo netflix">
        </div>
        <form >

          <input class="input" type="text" placeholder="Search Movies"
          v-model="searchMovies">

          <button type="submit" 
            @click.prevent="$emit('listen', searchMovies)">
            Inizia <i class="fa-solid fa-chevron-right"></i>
          </button>

        </form>
      </div>
    </header>
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




<style scoped lang="scss">
header {
  position: fixed;
  width: 100%;
  margin: auto;
  z-index: 1;
}


.boxUno {
  display: flex;
  justify-content: space-between;
  align-items: center;
  max-width: 100%;
  margin: auto;
  background-color: rgba(255, 0, 0, 0);
  padding: 10px 70px 10px 70px;
  // border: 5px solid rgb(255, 255, 255);
}

.logoNetflix {
  width: 30%;
}

form {
  display: flex;
  // text-align: center;

  .input {
    padding: 20px;
    border: none;
    display: flex;
    text-align: center;
    border-right: 1px solid rgb(28, 28, 28);
    border-top-left-radius: 3px;
    border-bottom-left-radius: 3px;
  }
  ::placeholder {
    color: rgba(255, 0, 0, 0.445);
  }

  input:focus{
    outline:none;
    color: rgb(255, 255, 255);
    background-color: rgba(48, 8, 8, 0.692);
    text-transform: uppercase;
  }

  button {
    background-color: red;
    border: none;
    padding: 10px 30px 10px 30px;
    color: white;
  }
}


</style>
