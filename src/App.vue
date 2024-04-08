<script>
  //axios
  import axios from 'axios';
  //axios

  import Jumbotron from './components/Jumbotron.vue';
  import Main from './components/Main.vue';
  import Footer from './components/Footer.vue';

  export default {
    components:{
      Jumbotron,
      Main,
      Footer
    },
    
  }
</script>


<template>
  <div class="d-flex flex-column align-items-center">
    <Jumbotron class="w-100" />
    <Main />
    <Footer />
  </div>
</template>


<style lang="scss">
  @use './assets/scss/main.scss';


</style>