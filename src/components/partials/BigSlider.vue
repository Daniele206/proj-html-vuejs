<script>
  import { dataBase } from '../../data/data';

  export default {
    data(){
      return{
        dataBase
      }
    }
  }
</script>



<template>
  <div class="bg d-center">
    <div class="my_container-m d-flex align-items-center">
      <div class="my_card">
        <div class="my-card-padding">
          <div class="price">{{ dataBase.mainBigSlider.price }}</div>
          <h2 class="main-spot text-uppercase">{{ dataBase.mainBigSlider.mainSpot }}</h2>
          <div class="text">{{ dataBase.mainBigSlider.text }}</div>
          <button class="btn btn-outline-light rounded-0 my_btn text-uppercase" >{{ dataBase.mainBigSlider.textBtn }}</button>
        </div>
      </div>
    </div>
  </div>
</template>


<style lang="scss" scoped>
@use '../../assets/scss/variables' as *;

.bg{
  background-image: url(/public/hero42x.jpg);
  width: 100%;
  aspect-ratio: 21/10;
  background-size: 100%;
  background-position: center;
  .my_card{
    background-color: $my-black;
    color: $my-white;
    width: 550px;
    aspect-ratio: 17/20;
    .my-card-padding{
      position: relative;
      margin: 100px 85px;
    }
    .price{
      position: absolute;
      top: 20px;
      right: 0;
      font-family: "Kanit", sans-serif;
      color: $my-light-gray;
      font-size: 1.1rem;
    }
    .main-spot{
      font-family: "Bebas Neue", sans-serif;
      font-weight: 400;
      font-style: normal;
      font-size: 4.5rem;
      &::after{
      content: '';
      display: block;
      width: 65px;
      height: 0;
      border: 1px solid $my-light-gray;
      margin-top: 75px
    }
    }
    .text{
      color: $my-light-gray;
      font-family: Georgia, 'Times New Roman', Times, serif;
      font-size: 1.3rem;
      padding: 40px 0;
    }
    .my_btn{
      font-family: "Kanit", sans-serif;
      font-size: .9rem;
      font-weight: 600;
      letter-spacing: 2px;
      padding: 10px 30px;
    }
  }
}

</style>