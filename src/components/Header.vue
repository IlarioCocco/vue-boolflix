<template>
    <header>
      <div class="boxUno">
        <div>
          <img class="logoNetflix" src="../assets/img/netflixLogoTipo.png" alt="logo netflix">
        </div>
        <form>
          
          <select class="select" name="category" id="category">
            <option value="all">All</option>
            <option value="Movies">Movies</option>
            <option value="Films">Films</option>
          </select>

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
  padding: 5px 50px 5px 50px;
  // border: 5px solid rgb(255, 255, 255);
}

.logoNetflix {
  width: 30%;
}

form {
  display: flex;
  // text-align: center;
  font-size: 15px;

  .input {
    padding: 20px;
    border: none;
    display: flex;
    text-align: center;
    border-right: 1px solid rgb(28, 28, 28);
    border-top-left-radius: 3px;
    border-bottom-left-radius: 3px;
    font-size: 15px;
  }
  ::placeholder {
    color: rgba(255, 0, 0, 0.445);
  }

  .select {
    border: none;
    outline:none;
    color: rgb(255, 255, 255);
    background-color: rgba(109, 0, 0, 0.534);
    padding: 10px 20px 10px 30px;
    margin-right: 15px;
    border-radius: 3px;
    font-size: 15px;
  }

  .input:focus{
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
    border-top-right-radius: 3px;
    border-bottom-right-radius: 3px;
    font-size: 15px;

    .fa-chevron-right {
      padding-left: 15px;
    }
  }
}


</style>
