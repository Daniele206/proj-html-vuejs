<script>
  import { dataBase } from '../data/data';
  import TheBTab from './partials/TheBTab.vue';
  import UnExp from './partials/UnExp.vue';

  export default {
    components:{
      UnExp,
      TheBTab,
    },

    data(){
      return{
        dataBase
      }
    }
  }
</script>


<template>
  <main class="d-flex flex-column align-items-center w-100">
    <UnExp 
    :preText1="dataBase.mainUnExp.preText1"
    :text1="dataBase.mainUnExp.text1"
    :mainSpot="dataBase.mainUnExp.mainSpot"
    :text2="dataBase.mainUnExp.text2"
    :sushiCard="dataBase.mainUnExp.sushiCard"
    />
    <TheBTab />
  </main>
</template>


<style lang="scss" scoped>
  @use '../assets/scss/variables' as *;

</style>