<script>
  import { dataBase } from '../../data/data';
  import CardMenues from './CardMenues.vue';

  export default {
    components:{
      CardMenues
    },

    data(){
      return{
        dataBase
      }
    },

    methods:{
      isCenter(i){
        if (i === 0 || i === 2){
          return 'lateral_m'
        }else if (i === 1){
          return 'central_m'
        }
      }
    }
  }
</script>


<template>
  <div class="menues_container d-flex">
    <CardMenues
    v-for="(menu, i) in dataBase.mainMenues"
    :key="i"
    :cardImg="menu.menuImg"
    :title="menu.title"
    :products="menu.products"
    :class="isCenter(i)"
    />
  </div>
</template>


<style lang="scss" scoped>
  @use '../../assets/scss/variables' as *;

  .central_m{
    margin-bottom: 55px;
  }

  .lateral_m{
    margin-top: 55px;
  }

  .menues_container{
    margin: 135px 0;
  }
</style>