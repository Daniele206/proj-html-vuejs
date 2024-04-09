<script>
  import { dataBase } from '../data/data';
  import MultiTab from './partials/MultiTab.vue';
  import TheBTab from './partials/MultiTab.vue';
  import UnExp from './partials/UnExp.vue';

  export default {
    components:{
      UnExp,
      MultiTab,
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
    <MultiTab 
      :title="dataBase.mainTheBTab.title"
      :mainSpot="dataBase.mainTheBTab.mainSpot"
      :fsMs="dataBase.mainTheBTab.fsMainSpot"
      :text="dataBase.mainTheBTab.text"
      :textBtn="dataBase.mainTheBTab.textBtn"
      :img="dataBase.mainTheBTab.img"
    />
    <MultiTab 
      :title="dataBase.mainTakeOut.title"
      :mainSpot="dataBase.mainTakeOut.mainSpot"
      :fsMs="dataBase.mainTakeOut.fsMainSpot"
      :text="dataBase.mainTakeOut.text"
      :textBtn="dataBase.mainTakeOut.textBtn"
      :icoBtn="dataBase.mainTakeOut.icoBtn"
      :img="dataBase.mainTakeOut.img"
    />
  </main>
</template>


<style lang="scss" scoped>
  @use '../assets/scss/variables' as *;

</style>