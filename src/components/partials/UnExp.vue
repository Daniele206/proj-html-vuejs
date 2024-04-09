<script>
  export default {
    
  }
</script>


<template>
  <div class="un-exp my_container-m">
    <div class="d-flex flex-wrap">
      <div class="w-50 un-info debug py-5">
        <div>Lorem ipsum dolor sit amet consectetur adipisicing elit. Maiores voluptatem asperiores, ea explicabo fugiat voluptatum suscipit ratione sunt iste, praesentium numquam labore consequuntur temporibus repellendus laudantium debitis, blanditiis voluptates reiciendis.</div>
        <h3 class="py-5">Lorem ipsum dolor sit amet consectetur adipisicing elit.</h3>
        <div>Lorem ipsum dolor sit amet consectetur adipisicing elit. Nihil sequi aspernatur consectetur ad neque eius consequuntur! Illo odit, eaque nam exercitationem quod natus quisquam ad illum tempora, aspernatur distinctio vero?</div>
        <img class="w-signature pt-3" src="/public/signature.jpg" alt="">
      </div>
      <div class="w-50 debug d-flex justify-content-end">
        <div class="my_card">
          <img class="card_img" src="/public/info22x.jpg" alt="">
          <div class="text-uppercase text_card-img">california rolls - $22</div>
        </div>
      </div>
    </div>
    <div>

    </div>
  </div>
</template>


<style lang="scss" scoped>
  @use '../../assets/scss/variables' as *;
  .w-signature{
    width: 35%;
  }

  .un-exp{
    margin: 130px 0;
    .un-info{
      padding-right: 4rem;
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