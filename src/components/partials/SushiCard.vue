<script>
  export default {
    
  }
</script>


<template>
  <div class="my_sushi_card px-5">
    <img src="/public/sushi-1.png" alt="">
    <h2 class="sushi-spot text-center">THE BEST TABLE IN TOWN</h2>
    <div class="suchi-text text-center p-text-btn">Sed aenean egestas ut aliquam turpis mauris, molestie. Vitae tellus tempor sem id tempus neque, tellus turpis turpis. Morbi tortor id gravida aliquet.</div>
    <button class="btn my_btn-outline-gray rounded-0 text-uppercase">EXPLORE THE MENU</button>
  </div>
</template>


<style lang="scss" scoped>
@use '../../assets/scss/variables' as *;

.p-text-btn{
  padding-bottom: 30px;
}

.my_sushi_card{
  width: calc(100% / 3);
  display: flex;
  flex-direction: column;
  align-items: center;
  .sushi-spot{
    font-family: "Bebas Neue", sans-serif;
    font-weight: 400;
    font-style: normal;
    padding: 40px 0 20px 0;
    &::after{
      content: '';
      display: block;
      margin: 0 auto;
      width: 60px;
      height: 0;
      border: 1px solid $my-light-gray;
      margin-top: 20px
    }
  };
  .suchi-text{
    color: $my-dark-gray;
    font-family: Georgia, 'Times New Roman', Times, serif;
    font-size: 1.1rem;
  }
  .my_btn-outline-gray{
    border: 1px solid $my-light-gray;
    font-family: "Kanit", sans-serif;
    font-size: .9rem;
    letter-spacing: 2px;
    padding: 10px 30px;
    &:hover{
      border-color: $my-black;
    };
  };
}

</style>