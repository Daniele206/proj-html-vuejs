<script>

  import InfoEBtn from './InfoEBtn.vue';

  export default {
    components:{
      InfoEBtn
    },

    props:{
      title: String,
      mainSpot: String,
      fsMs: String,
      text: String,
      textBtn: String,
      img: String,
      icoBtn: String
    },
  }
</script>


<template>
  <div class="bg-black w-100 d-flex justify-content-center img-bg" :style="`background-image: url(/public/${img});`">
    <div class="my_container total-pd d-flex justify-content-end">
      <InfoEBtn 
      class="text-white"
      :title="title"
      :mainSpot="mainSpot"
      :fsMs="fsMs"
      :text="text"
      :textBtn="textBtn"
      :icoBtn="icoBtn"
      />
    </div>
  </div>
</template>


<style lang="scss" scoped>
@use '../../assets/scss/variables' as *;

.total-pd{
  padding-top: 200px;
  padding-bottom: 180px;
}

.img-bg{
  background-size: 1150px;
  background-repeat: no-repeat;
}

</style>