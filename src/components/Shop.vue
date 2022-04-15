<template>
  <footer>
      <section class="boxFooter">
            <div>
                Shop      
            </div>
            <div>
                Shop     
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
    border-top: 8px solid rgb(42, 42, 42);
}

.boxFooter {
    width: 50%;
    margin: auto;
    display: flex;
    justify-content: space-between;
    align-content: center;
    background-color: black;
    padding: 70px 0px;
    color: rgb(255, 255, 255);
    font-size: 30px;
    // border: 5px solid rgb(47, 92, 224)
}

</style>