<script>
  export default {
    
  }
</script>


<template>
  <header>
    <div class="my-container">
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
    </div>
  </header>
</template>


<style lang="scss" scoped>
  @use '../../assets/scss/variables' as *;

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