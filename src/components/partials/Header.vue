<script>
  export default {
    
  }
</script>


<template>
  <header>
    <div class="my_container">
      <div class="row">
        <div class="col col-5">
          <img src="/public/logo-restaurant.png" alt="">
        </div>
        <div class="rigth-col col col-7 justify-content-end">
          <ul class="d-flex list-unstyled fw-bold">
            <li class="px-3"><a href="#">Home</a></li>
            <li class="px-3"><a href="#">Culinary History</a></li>
            <li class="px-3"><a href="#">Our Team</a></li>
            <li class="px-3"><a href="#">Our Menu</a></li>
            <li class="px-3"><a href="#" class="new-flag">Takeout</a></li>
            <li class="px-3"><a href="#">Bulletin</a></li>
            <li class="px-3"><a href="#">Reservations</a></li>
            <li class="px-3"><a href="#"><i class="fa-solid fa-cart-shopping"></i></a></li>
          </ul>
        </div>
      </div>
      <div class="box-flag-container d-flex flex-column">
        <div v-for="i in 2" class="box-flag mt-2">
          <div v-if="i === 1" class="box-content"><i class="fa-solid fa-paper-plane my-blue"></i></div>
          <div v-else-if="i === 2" class="box-content box-content-price fs-3 fw-bold my_text_green">
          <div class="fs-5 mb-1 pb-2">$</div>
          <div>39</div>
          </div>
          <div v-if="i === 1" class="box-text text-center">Demos</div>
          <div v-else-if="i === 2" class="box-text text-center">On Sale</div>
        </div>
      </div>
    </div>
  </header>
</template>


<style lang="scss" scoped>
  @use '../../assets/scss/variables' as *;

  .my_text_green{
    color: #63BA79;
  }

  .my-blue{
    color: $my-matt-blue;
  }

  .new-flag::after{
    font-size: .7rem;
    content: 'New';
    margin-left: 10px;
    padding: 3px 6px;
    border: 1px solid $my-darck-gray;
    border-radius: 2px;
  }

  header{
    color: $my-white;
    padding-top: 40px;
    height: 180px;
    width: 100%;
    position: fixed;
    display: flex;
    justify-content: center;
    background: linear-gradient(rgb(0, 0, 0) -25%, rgba(0, 0, 0, 0));
    .box-flag-container{
      position: absolute;
      top: 140px;
      right: 20px;
      .box-flag{
        background-color: $my-white;
        width: 65px;
        aspect-ratio: 1;
        border-radius: 8px;
        color: $my-darck-gray;
        box-shadow: 0 0 4px $my-black;
        .box-content{
          height: 60%;
          display: flex;
          justify-content: center;
          align-items: center;
          padding-top: 10px;
        }
        .box-content-price{
          font-family: "Poppins", snas-serif;
        }
        .box-text{
          font-size: 0.8rem;
          font-weight: bold;
        }
    }
    }
    .col{
      display: flex;
      align-items: center;
      ul{
        padding: 0;
        margin: 0;
        li{
          a{
            color: $my-light-gray;
            text-decoration: none;
          }
        }
      }
    }
  }


</style>