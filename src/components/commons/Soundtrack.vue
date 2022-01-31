<template>
  <div class="soundtrack text-center col-2 m-3">
    <div class="containerImg m-auto p-3">
      <img 
      :src="info.poster" 
      :alt="info.title"
      class="img-fluid mb-3">
    </div>
      <h4 class="p-2 text-uppercase">{{info.title}}</h4>
      <div class="author">{{info.author}}</div>
      <div class="year">{{info.year}}</div>

  </div>
</template>

<script>

export default {
  name: 'Soundtrack',
 
  props: {
      info: Object
    
  }
}
</script>


<style scoped lang="scss">
@import "../../assets/style/global.scss";
.soundtrack{
    background-color: $background-color ;
    .containerImg{
      height: 206px;
      width: 181px;
      overflow: hidden;
      img{
        height: 100%;
        object-fit: cover;
      }
    }
    h4{
      color:$title-color;
    }
    .author,
    .year{
      color:#6c6c6d;
    }

    
   
}

</style>
