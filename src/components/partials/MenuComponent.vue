<script>
  export default {
    props:{
      name: String,
      description: String,
      price: String,
      img: String
    },

    methods:{
      isDarck(bol){
        if (bol !== false){
          return 'is-dark'
        }
      }
    }
    
  }
</script>


<template>
  <div class="product" :class="isDarck(img)">
    <div class="price">{{ price }}</div>
    <h2 class="name">{{ name }}</h2>
    <div class="description">{{ description }}</div>
  </div>
</template>


<style lang="scss" scoped>
  @use '../../assets/scss/variables' as *;

  .product{
    position: relative;
    padding: 20px 0;
    .name{
      font-family: "Bebas Neue", sans-serif;
      font-weight: 400;
      font-style: normal;
    }
    .description{
      color: $my-dark-gray;
      font-family: Georgia, 'Times New Roman', Times, serif;
      font-size: 1.2rem;
      line-height: 2.2rem;
    }
    .price{
      font-family: "Kanit", sans-serif;
      color: $my-dark-gray;
      position: absolute;
      top: 25px;
      right: 0;
    }
  };
  
  .is-dark{
    .description{
      color: $my-light-gray;
    }
    .price{
      color: $my-light-gray;
    }
  }

</style>