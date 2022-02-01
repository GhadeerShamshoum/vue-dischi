<template>
    <select v-model="selectGenre"
     @change="$emit('filter',selectGenre)" 
    class="inputSelect ms-4" name="genre" id="pet-select">
        <option value="">Please choose a genre</option>
        <option value="Rock">Rock</option>
        <option value="Jazz">Jazz</option>
        <option value="Pop">Pop</option>
        <option value="Metal">Metal</option>
    </select>
</template>

<script>

export default {
    name: 'Options',
    components: {
    
    },
    data() {
      return {
         selectGenre:"",
          
          
      }
    }

   
      
}
 
</script>

<style lang="scss" scoped>
.inputSelect{
    height: 30px;
    width: 250px;
}
</style>