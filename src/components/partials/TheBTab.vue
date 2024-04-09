<script>
  import { dataBase } from '../../data/data';

  import InfoEBtn from './InfoEBtn.vue';

  export default {
    components:{
      InfoEBtn,
    },

    data(){
      return{
        dataBase
      }
    }
  }
</script>


<template>
  <div class="bg-black w-100 d-flex justify-content-center img-bg">
    <div class="my_container total-pd d-flex justify-content-end">
      <InfoEBtn 
      class="text-white"
      :title="dataBase.mainTheBTab.title"
      :mainSpot="dataBase.mainTheBTab.mainSpot"
      :fsMs="dataBase.mainTheBTab.fsMainSpot"
      :text="dataBase.mainTheBTab.text"
      :textBtn="dataBase.mainTheBTab.textBtn"
      />
    </div>
  </div>
</template>


<style lang="scss" scoped>
@use '../../assets/scss/variables' as *;

.total-pd{
  padding-top: 200px;
  padding-bottom: 180px;
}

.img-bg{
  background-image: url(/public/slider32x.jpg);
  background-size: 1150px;
  background-repeat: no-repeat;
}

</style>