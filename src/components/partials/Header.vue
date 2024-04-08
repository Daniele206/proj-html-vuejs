<script>
  export default {
    
  }
</script>


<template>
  <header class="my-container d-flex align-items-center">
    <div class="container-fluid">
      <div class="row">
        <div class="col col-5">logo</div>
        <div class="col col-7 justify-content-end">
          <ul class="d-flex list-unstyled">
            <li class="px-3"><a href="#">ciao</a></li>
            <li class="px-3"><a href="#">ciao</a></li>
            <li class="px-3"><a href="#">ciao</a></li>
            <li class="px-3"><a href="#">ciao</a></li>
            <li class="px-3"><a href="#">ciao</a></li>
            <li class="px-3"><a href="#">ciao</a></li>
            <li class="px-3"><a href="#">ciao</a></li>
            <li class="px-3"><a href="#"><i class="fa-solid fa-cart-shopping"></i></a></li>
          </ul>
        </div>
      </div>
    </div>
  </header>
</template>


<style lang="scss" scoped>
  @use '../../assets/scss/variables' as *;

  header{
    height: 140px;
    position: fixed;
    border: 1px solid black;
    .col{
      border: 1px solid black;
      display: flex;
      align-items: center;
      ul{
        padding: 0;
        margin: 0;
        li{
          a{
            text-decoration: none;
          }
        }
      }
    }
  }


</style>