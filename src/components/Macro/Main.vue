<template>
  <main class="container m-auto mt-5 mb-5">
      <div class="row">
          <div class="col">
              <PlayList/>
          </div>
      </div>
  </main>
</template>

<script>
import PlayList from "../sections/PlayList.vue"
export default {
  name: 'Main',
  components: {
      PlayList
  },
  props: {
    
  }
}
</script>


<style scoped lang="scss">
@import "../../assets/style/global.scss";
.container{
  width: 1200px;
  margin: 20px 0;
  
  

}


</style>
