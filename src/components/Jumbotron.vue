
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
    <div id="jumbotron-contet" class="my-container d-flex">
      <div class="befor-jum-info"></div>
      <div class="w-25">
        <h3 class="pb-5">titolo</h3>
        <h2 class="main-spot text-uppercase pb-5 pt-3">parola parola parolaLunga</h2>
        <div class="pb-5 pt-3">Lorem ipsum dolor sit amet consectetur adipisicing elit. Vitae fuga rerum nobis harum doloremque recusandae architecto repellendus ab voluptates quasi.</div>
        <button class="mb-jum mt-3">bottone</button>
      </div>
    </div>
  </div>
</template>


<style lang="scss" scoped>
  @use '../assets/scss/variables' as *;

  #jumbotron{
    background-image: url(/public/slider52x.jpg);
    background-size: contain;
    background-repeat: no-repeat;
    background-position: right;
    background-color: $my-black;
  }

  #jumbotron-contet{
    color: $my-white;

    .mb-jum{
      margin-bottom: 10rem;
    }

    .befor-jum-info{
      border: 0.5px solid $my-light-gray;
      width: 50px;
      height: 0;
      margin-top: 0.8rem;
      margin-right: 55px;
    }
    .main-spot{
      font-size: 3.5rem;
      font-weight: bold;
    }
  }

</style>