<script>
  import ShortAbUsCard from './ShortAbUsCard.vue'


  export default {
    props:{
      data: Object,
    },

    components:{
      ShortAbUsCard
    }
  }
</script>


<template>
  <div class="long-card">
    <ShortAbUsCard 
    :img="data.img"
    :title="data.title"
    :mainSpot="data.mainSpot"
    :text1="data.text1"
    :text2="data.text2"
    :textBtn="data.textBtn"
    :width="data.width"
    />
  </div>
</template>


<style lang="scss" scoped>
@use '../../assets/scss/variables' as *;

.long-card{
  background-image: url(/public/blog72x.jpg);
  background-size: 53%;
  background-repeat: no-repeat;
  width: 100%;
  display: flex;
  justify-content: flex-end;
}

</style>