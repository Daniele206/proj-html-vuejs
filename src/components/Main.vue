<script>
  import { dataBase } from '../data/data';
  import UnExp from './partials/UnExp.vue'

  export default {
    components:{
      UnExp,
    },

    data(){
      return{
        dataBase
      }
    }
  }
</script>


<template>
  <main class="d-flex flex-column align-items-center">
    <UnExp 
    :preText1="dataBase.mainUnExp.preText1"
    :text1="dataBase.mainUnExp.text1"
    :mainSpot="dataBase.mainUnExp.mainSpot"
    :text2="dataBase.mainUnExp.text2"
    />
  </main>
</template>


<style lang="scss" scoped>
  @use '../assets/scss/variables' as *;

</style>