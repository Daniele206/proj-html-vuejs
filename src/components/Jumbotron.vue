
<script>
  import Header from './partials/Header.vue'

  export default {
    components:{
      Header
    }
    
  }
</script>


<template>
  <div id="jumbotron" class="d-flex flex-column align-items-center">
    <Header />
    <div id="jumbotron-contet" class="my-container">
      Jumbotron
    </div>
  </div>
</template>


<style lang="scss" scoped>
  @use '../assets/scss/variables' as *;

  #jumbotron-contet{
    background-color: $my-black;
    padding-top: 140px;
    border: 1px solid black;
  }

</style>