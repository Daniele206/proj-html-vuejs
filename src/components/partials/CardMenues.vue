<script>
  import MenuComponent from './MenuComponent.vue';

  export default {
    components:{
      MenuComponent,
    },
    
    props:{
      cardImg: String,
      title: String,
      products: Array,
    },

    methods:{
      isShadow(bol){
        if (bol !== false){
          return 'my_shadow'
        }
      }
    }
    
  }
</script>


<template>
  <div class="my_card_bg" :style="`background-image: url(/public/${cardImg});`">
    <div :class="isShadow(cardImg)">
      <div class="my-card-menu-contet text-white">
        <h2 class="title">{{ title }}</h2>
        <MenuComponent
        v-for="(product, i) in products"
        :key="i"
        :name="product.name"
        :description="product.description"
        :price="product.price"
        :img="cardImg"
        class="color-text"
        />
      </div>
    </div>
  </div>
</template>


<style lang="scss" scoped>
  @use '../../assets/scss/variables' as *;

  .my_card_bg{
    width: 560px;
    aspect-ratio: 10/17;
    background-color: $my-light2-gray;
    background-size: 100%;
    background-position: center;
    .my-card-menu-contet{
      padding: 110px 100px;
      .title{
        color: $my-black;
        font-family: "Bebas Neue", sans-serif;
        font-weight: 400;
        font-style: normal;
        font-size: 3rem;
        padding-bottom: 40px;
      }
      .color-text{
        color: $my-black;
      }
    }
    .my_shadow{
      height: 100%;
      width: 100%;
      background: linear-gradient(rgb(0, 0, 0) 27%, rgba(0, 0, 0, 0));
      .my-card-menu-contet{
        .title{
          color: $my-white;
        }
        .color-text{
          color: $my-white;
        }
      }
    }
  }
</style>