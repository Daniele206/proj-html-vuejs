<script>
  import SushiCard from './SushiCard.vue';

  export default {
    components:{
      SushiCard
    },

    props:{
      preText1:String,
      text1: String,
      mainSpot: String,
      text2: String,
    }
    
  }
</script>


<template>
  <div class="un-exp my_container-m">
    <div class="d-flex flex-wrap">
      <div class="w-50 un-info py-5">
        <div class="un-info-card">
          <div class="un-exp-text"><strong>{{ preText1 }}</strong>{{ text1 }}</div>
          <h3 class="py-5 main-spot">{{ mainSpot }}</h3>
          <div class="un-exp-text">{{ text2 }}</div>
          <img class="w-signature pt-3" src="/public/signature.jpg" alt="">
        </div>
      </div>
      <div class="w-50 d-flex justify-content-end">
        <div class="my_card">
          <img class="card_img" src="/public/info22x.jpg" alt="">
          <div class="text-uppercase text_card-img">california rolls - $22</div>
        </div>
      </div>
    </div>
    <div class="sushi-pt">
      <SushiCard />
    </div>
  </div>
</template>


<style lang="scss" scoped>
  @use '../../assets/scss/variables' as *;
  .w-signature{
    width: 35%;
  }

  .sushi-pt{
    padding-top: 170px;
  }

  .un-exp{
    margin: 130px 0;
    .un-info{
      padding-right: 4rem;
      .un-info-card{
        width: 90%;
        .main-spot{
          font-family: "Bebas Neue", sans-serif;
          font-size: 4.8rem;
        }
        .un-exp-text{
          font-family: Georgia, 'Times New Roman', Times, serif;
          font-size: 1.2rem;
          letter-spacing: 0.01rem;
          line-height: 2rem;
          color: $my-dark-gray;
        }
      }
    }
    .my_card{
      background-color: black;
      position: relative;
      width: 660px;
      aspect-ratio: 12.7/16;
      overflow: hidden;
      .card_img{
        mask-image: linear-gradient(black 75%, transparent );
      }
      .text_card-img{
        font-family: "Kanit", sans-serif;
        color: $my-white;
        position: absolute;
        bottom: 20px;
        left: 50%;
        transform: translatex(-50%);
        letter-spacing: .1rem;
      }
    }
  }
</style>