<template>
  <section class="container">
      <div class="row">
          <div class="d-flex flex-wrap" >
            <Soundtrack v-for="soundtrack in playlistArray "
            :key="soundtrack"
            :info="soundtrack"
            />
          </div>
          
      </div>
  </section>
</template>

<script>
import axios from "axios"
import Soundtrack from "../commons/Soundtrack.vue"
export default {
  name: 'PlayList',
  data() {
      return {
          apiURL: "https://flynn.boolean.careers/exercises/api/array/music",
          playlistArray: []
      }
  },
  components: {
      Soundtrack
  },
  created(){
      this.getPlayList();
  },
  methods: {
      getPlayList() {
          axios
                .get(this.apiURL)
                .then( (risponde) => {
                    // handle success
                    this.playlistArray = risponde.data.response;
                    
                })
                .catch(function (error) {
                    // handle error
                    console.log(error);
                });

      }
  }

}
</script>


<style scoped lang="scss">
.card{
    margin: 10px; 
    background-color: transparent;
    
}


</style>
