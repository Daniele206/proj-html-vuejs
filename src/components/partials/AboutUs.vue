<script>
  import { dataBase } from '../../data/data';
  import LongAbUsCard from './LongAbUsCard.vue';
  import ShortAbUsCard from './ShortAbUsCard.vue';

  export default {
    components:{
      LongAbUsCard,
      ShortAbUsCard
    },

    data(){
      return{
        dataBase
      }
    }
    
  }
</script>


<template>
  <div class="about-container d-center flex-column w-100">
    <h2 class="title">What critics are sauing about us</h2>
    <div class="d-center flex-column w-100">
      <div class="my_container-m">
        <LongAbUsCard 
        :data="dataBase.mainAbUs.longCard"
        />
      </div class="my_container-m ">
      <div class="my_card my_container-m mt-5">
        <div v-for="(card, i) in dataBase.mainAbUs.shortCard" :class="{'justify-content-end' : i === 1}" class="w-50 d-flex">
          <ShortAbUsCard
          :img="card.img"
          :title="card.title"
          :mainSpot="card.mainSpot"
          :text1="card.text1"
          :text2="card.text2"
          :textBtn="card.textBtn"
          :width="card.width"
          />
        </div>
      </div>
    </div>
  </div>
</template>


<style lang="scss" scoped>
@use '../../assets/scss/variables' as *;

.about-container{
    padding-top: 130px;
    padding-bottom: 110px;
    .title{
      font-family: Georgia, 'Times New Roman', Times, serif;
      font-size: 3rem;
      &::after{
      content: '';
      display: block;
      margin: 0 auto;
      width: 70px;
      height: 0;
      border: 1px solid $my-light2-gray;
      margin-top: 30px;
      margin-bottom: 40px;
    }
    }
  }

  .my_card{
    display: flex;
    justify-content: space-between;
  }
</style>