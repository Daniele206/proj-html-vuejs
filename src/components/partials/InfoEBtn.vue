<script>
  export default {
    props:{
      title: String,
      maniSpot: String,
      text: String,
      textBtn: String
    }
    
  }
</script>


<template>
  <div class="d-flex">
    <div class="befor-jum-info"></div>
    <div class="w-25">
      <h3 class="pb-4 title text-uppercase">the best table in town</h3>
      <h2 class="main-spot text-uppercase pb-4 pt-2">fine dining experience</h2>
      <div class="text pb-5 pt-2">
        Pelentesque vitae viverra risus, sagittis.
        <br>
        Venenatis ridiculus sclerique nisi in urna
        <br>
        nulla. Sit tempor a et nisl, ac felis.
      </div>
      <button class="my-btn mt-4 btn btn-outline-light rounded-0 text-uppercase">explore the menu</button>
    </div>
  </div>
</template>


<style lang="scss" scoped>
  @use '../../assets/scss/variables' as *;

  .befor-jum-info{
    border: 0.5px solid $my-light-gray;
    width: 50px;
    height: 0;
    margin-top: 0.8rem;
    margin-right: 55px;
  }
  
  .title{
    font-family: "Kanit", sans-serif;
    padding-top: .25rem;
    font-size: .9rem;
    font-weight: 600;
    letter-spacing: 2px;
    color: $my-light-gray;
  }
  
  .main-spot{
    font-size: 5.8rem;
    font-family: "Bebas Neue", sans-serif;
    font-weight: 400;
    font-style: normal;
  }
  
  .text{
    color: $my-light-gray;
    font-family: Georgia, 'Times New Roman', Times, serif;
    font-size: 1.3rem;
  }

  .my-btn{
    margin-bottom: 12rem;
    font-family: "Kanit", sans-serif;
    font-size: .9rem;
    font-weight: 600;
    letter-spacing: 2px;
    padding: 10px 30px;
  }
  
</style>