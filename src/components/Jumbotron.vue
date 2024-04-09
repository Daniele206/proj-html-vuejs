
<script>
  import Header from './partials/Header.vue';
  import InfoEBtn from './partials/InfoEBtn.vue';
  import { dataBase } from '../data/data';

  export default {
    components:{
      Header,
      InfoEBtn
    },

    data(){
      return{
        dataBase,
      }
    }
    
  }
</script>


<template>
  <div id="jumbotron" class="d-flex flex-column align-items-center">
    <Header />
    <div id="jumbotron-contet" class="my_container">
      <InfoEBtn 
      :title="dataBase.jumbotron.title"
      :mainSpot="dataBase.jumbotron.mainSpot"
      :fsMs="dataBase.jumbotron.fsMainSpot"
      :text="dataBase.jumbotron.text"
      :textBtn="dataBase.jumbotron.textBtn"
      />
    </div>
  </div>
</template>


<style lang="scss" scoped>
  @use '../assets/scss/variables' as *;

  #jumbotron{
    background-image: url(/public/slider52x.jpg);
    background-size: contain;
    background-repeat: no-repeat;
    background-position: right;
    background-color: $my-black;
  }

  #jumbotron-contet{
    padding-top: 260px;
    color: $my-white;
  }

</style>