<script>
  export default {
    props:{
      img: String,
      title: String,
      text: String,
    }
    
  }
</script>


<template>
  <div class="my-card">
    <div class="img" :style="`background-image: url(/public/${img});`">
      <div class="shadow-hover">
        <div class="cont-img d-center h-100">
          <div class="d-center flex-column hover-text">
            <i class="fa-solid fa-link"></i>
            <h3 class="name-card">{{ title }}</h3>
            <div class="text">News</div>
          </div>
        </div>
      </div>
    </div>
    <div class="text_info d-center flex-column">
      <h3 class="name-card">{{ title }}</h3>
      <div class="text">{{ text }}</div>
    </div>
  </div>
</template>


<style lang="scss" scoped>
  @use '../../assets/scss/variables' as *;
  .hover-text{
    color: $my-white;
    display: none;
  }

  .name-card{
    font-family: "Bebas Neue", sans-serif;
    font-weight: 400;
    font-style: normal;
    font-size: 2rem;
  }
  .text{
    font-family: Georgia, 'Times New Roman', Times, serif;
    font-size: .8rem;
  }
  .my-card{
    width: 430px;
    aspect-ratio: 9/16;
    margin: 0 20px;
    &:hover .hover-text{
      display: flex;
    }
    .text_info{
      height: 17%;
      transition: 0.3s;
      .text{
        color: $my-dark-gray;
      }
    }
    &:hover .text_info{
      transition: 0.3s;
      height: 0;
      .name-card{
        display: none;
      }
      .text{
        display: none;
      }
    }
    &:hover .img{
      transition: 0.3s;
      height: 100%;
      cursor: pointer;
    }
    .img{
      height: 83%;
      background-size: 155%;
      background-position: top;
      background-repeat: no-repeat;
      transition: 0.3s;
      background-color: $my-black;
      .shadow-hover{
        width: 100%;
        height: 100%;
        &:hover{
          background: linear-gradient(rgb(0, 0, 0) -15%, rgba(0, 0, 0, 0));
        }
      }
    }
  }

</style>