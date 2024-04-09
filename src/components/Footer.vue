<script>
  import { dataBase } from '../data/data';

  export default {
    data(){
      return{
        dataBase
      }
    }
  }
</script>


<template>
  <footer class="d-flex flex-column justify-content-end align-items-center ">
    <div class="info-footer d-flex justify-content-end align-items-center  text-center flex-column">
      <img class="pb-5" src="/public/logo-restaurant.png" alt="">
      {{ dataBase.footer.text }}
      <div class="pt-5">
        <i class="fa-brands fa-facebook-f my_social d-center"></i>
      </div>
    </div>
    <div class="copy d-center">
      {{ dataBase.footer.copy }}
    </div>
  </footer>
</template>


<style lang="scss" scoped>
  @use '../assets/scss/variables' as *;

  .my_social{
    background: $my-white;
    color: $my-black;
    width: 50px;
    aspect-ratio: 1;
    border-radius: 50%;
    margin-bottom: 11.5rem;
  }

  footer{
    font-family: Georgia, 'Times New Roman', Times, serif;
    color: $my-white;
    background-image: url(/public/footer2x.jpg);
    width: 100%;
    aspect-ratio: 20/8;
    background-size: 100%;
    background-position: top;
    background-repeat: no-repeat;
    .info-footer{
      height: 90%;
      font-size: 1.3rem;
      width: 33%;
      color: $my-light-gray;
    }
    .copy{
      width: 100%;
      font-size: .8rem;
      background-color: $my-black;
      height: 10%;
    }
  }

</style>