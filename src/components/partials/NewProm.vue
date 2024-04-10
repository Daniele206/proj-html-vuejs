<script>
  import { dataBase } from '../../data/data';
  import PromCard from './PromCard.vue';

  export default {
    components:{
      PromCard
    },
    
    data(){
      return{
        dataBase
      }
    }

  }
</script>


<template>
  <div class="news-container d-center flex-column">
    <h2 class="title">Latest news & promotions</h2>
    <div class="d-center">
      <PromCard
      v-for="(prom, i) in dataBase.mainNewProm.card"
      :key="i"
      :img="prom.img"
      :title="prom.cardTitle"
      :text="prom.text"
      />
    </div>
  </div>
</template>


<style lang="scss" scoped>
  @use '../../assets/scss/variables' as *;

  .news-container{
    padding-top: 100px;
    padding-bottom: 80px;
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

</style>