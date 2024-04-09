<script>
  export default {
    
  }
</script>


<template>
  <div class="bg">
    <div class="slider">
      <img class="slider-img" src="/public/page52x.jpg" alt="">
      <div class="slider-text">Kung Pao Chicken - $32</div>
    </div>
  </div>
</template>


<style lang="scss" scoped>
  @use '../../assets/scss/variables' as *;

  .bg{
    background-color: $my-black;
    width: 100%;
    .slider{
      color: $my-white;
      position: relative;
      width: 100%;
      aspect-ratio: 11/4;
      background-size: cover;
      background-position: center;
      text-transform: uppercase;
      .slider-img{
        height: 100%;
        object-fit: cover;
        mask-image: linear-gradient(black 75%, transparent );
      }
      .slider-text{
        position: absolute;
        bottom: 0;
        left: 50%;
        transform: translateX(-50%);
        padding-bottom: 40px;
        font-family: "Kanit", sans-serif;
        letter-spacing: .1rem;
      }
    }
  }
</style>