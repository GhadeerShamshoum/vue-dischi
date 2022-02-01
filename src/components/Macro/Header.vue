<template>
  <header class="container-fluid">
    <div class="row">
      <div  class="d-flex align-items-center col-12">
        <Logo />
        
      </div>
    </div>
  </header>
</template>

<script>
import Logo from '../commons/Logo.vue';
export default {
  name: 'Header',
   components: {
      Logo
    },
  props: {
    
  }
}
</script>


<style scoped lang="scss">
@import "../../assets/style/global.scss";
.container-fluid{
  background-color: $background-color;
}

</style>
