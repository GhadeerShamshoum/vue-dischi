<template>
  <section class="container">
      <div v-if="!loading" class="row">
      <Options
      @filter="filterGenre" />
      <OptionsAuthor 
      @filter="filterArtist"/>
          <div class="d-flex flex-wrap" >
            <Soundtrack v-for="(soundtrack,index) in filteredGenres"
            :key="index"
            :info="soundtrack"
            />
          </div>
      </div>
      <Loader v-else/>
  </section>
</template>

<script>
import axios from "axios"
import Options from '../sections/Options.vue'
import Soundtrack from "../commons/Soundtrack.vue"
import Loader from "../commons/Loader.vue"
import OptionsAuthor from '../sections/OptionsAuthor.vue';
export default {
  name: 'PlayList',
  data() {
      return {
          apiURL: "https://flynn.boolean.careers/exercises/api/array/music",
          playlistArray: [],
          loading: true,
          newInput:'',
          
      }
  },
  components: {
      Soundtrack,
      Loader,
      Options,
      OptionsAuthor
  },
  created(){
      this.getPlayList();
  },
  computed: {
        filteredGenres(){
            if(this.newInput == ''){
                return this.playlistArray
            }
            else{

                return this.playlistArray.filter( (item) => {
                    return item.genre.includes(this.newInput)||item.author.includes(this.newInput)
                    
                });

            }
        },
        
    },
  methods: {
      filterGenre(selected){
          this.newInput = selected;
          console.log(this.newInput)
          
      },

      filterArtist(selected){
          this.newInput = selected;
          console.log(this.newInput)
          
      },

      getPlayList() {
          axios
                .get(this.apiURL)
                .then( (risponde) => {
                    // handle success
                    this.playlistArray = risponde.data.response;
                    this.loading = false;
                    
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
    min-width: 400px; 
    background-color: transparent;
    
}


</style>
