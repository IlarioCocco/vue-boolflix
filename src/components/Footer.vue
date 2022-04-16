<template>
  <footer>
      <section class="boxFooter">
            <div>
                Footer Netflix      
            </div>
            <div>
                Footer Netflix      
            </div>
      </section>
  </footer>
</template>

<script>
export default {
    name: 'Footer'

}
</script>


<style scoped lang="scss">

footer {
    background-color: black;
    border-top: 7px solid rgb(42, 42, 42);
}

.boxFooter {
    width: 60%;
    margin: auto;
    display: flex;
    justify-content: space-between;
    align-content: center;
    background-color: black;
    padding: 70px 0px;
    color: red;
    font-size: 50px;
    // border: 5px solid rgb(47, 92, 224)
}

</style>