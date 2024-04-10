<script>
  export default {
    props:{
      img: String,
      title: String,
      mainSpot: String,
      text1: String,
      text2: String,
      textBtn: String,
      width: String,
    },

    methods:{
      isShadow(bol){
        if (bol !== false){
          return 'is-shadow'
        }
      }
    }
    
  }
</script>


<template>
  <div class="shor-card" :style="`width: ${width}; background-image: url(/public/${img});`">
    <div class="w-100 h-100 my_box" :class="isShadow(img)">
      <div class="title">{{ title }}</div>
      <h2 class="main-spot">{{ mainSpot }}</h2>
      <div class="stars">
        <i v-for="i in 5" class="fa-solid fa-star pe-2"></i>
      </div>
      <div class="text">{{ text1 }}</div>
      <div v-if="text2 !== false" class="text text2">{{ text2 }}</div>
      <button class="btn btn-outline-light rounded-0 my_btn">{{ textBtn }}</button>
    </div>
  </div>
</template>


<style lang="scss" scoped>
@use '../../assets/scss/variables' as *;

  .shor-card{
    aspect-ratio: 23/27;
    background-color: $my-black;
    background-size: 100%;
    color: $my-white;
  }

  .my_box{
    padding: 140px;
  }

  .is-shadow{
    background: linear-gradient(rgb(0, 0, 0) 30%, rgba(0, 0, 0, 0));
  }

  .my_btn{
    font-family: "Kanit", sans-serif;
    font-size: .9rem;
    font-weight: 600;
    letter-spacing: 2px;
    padding: 10px 30px;
    margin-top: 40px;
  }

  .text{
    color: $my-light2-gray;
    font-family: Georgia, 'Times New Roman', Times, serif;
    font-size: 1.3rem;
    padding-bottom: 20px;
  }

  .title{
    font-family: "Kanit", sans-serif;
    padding-top: .25rem;
    font-size: .9rem;
    font-weight: 600;
    letter-spacing: 2px;
    color: $my-light-gray;
    padding-bottom: 40px;
  }

  .main-spot{
    font-family: "Bebas Neue", sans-serif;
    font-weight: 400;
    font-style: normal;
    font-size: 3.5rem;
  }

  .stars{
    padding-top: 30px;
    &::after{
      content: '';
      display: block;
      width: 70px;
      height: 0;
      border: 1px solid $my-light-gray;
      margin-top: 50px;
      margin-bottom: 40px;
    }
  }

</style>