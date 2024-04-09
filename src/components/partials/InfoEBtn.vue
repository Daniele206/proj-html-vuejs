<script>
  export default {
    
  }
</script>


<template>
  <div class="d-flex">
    <div class="befor-jum-info"></div>
    <div class="w-25">
      <h3 class="pb-5">titolo</h3>
      <h2 class="main-spot text-uppercase pb-5 pt-3">parola parola parolaLunga</h2>
      <div class="pb-5 pt-3">Lorem ipsum dolor sit amet consectetur adipisicing elit. Vitae fuga rerum nobis harum doloremque recusandae architecto repellendus ab voluptates quasi.</div>
      <button class="mb-jum mt-4 btn btn-outline-light rounded-0">bottone</button>
    </div>
  </div>
</template>


<style lang="scss" scoped>
  @use '../../assets/scss/variables' as *;

  .mb-jum{
    margin-bottom: 12rem;
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


</style>