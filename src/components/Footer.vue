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
      <div class="pt-5 d-flex">
        <a v-for="i in dataBase.footer.social" class="mx-2 my_social d-center" href="#"><i :class="i"></i></a>
      </div>
    </div>
    <div class="copy d-center">
      {{ dataBase.footer.copy }}
    </div>
  </footer>
</template>


<style lang="scss" scoped>
  @use '../assets/scss/variables' as *;

  a{
    text-decoration: none;
  }

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
    color: $my-light-gray;
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
    }
    .copy{
      width: 100%;
      font-size: .8rem;
      background-color: $my-black;
      height: 10%;
    }
  }

</style>