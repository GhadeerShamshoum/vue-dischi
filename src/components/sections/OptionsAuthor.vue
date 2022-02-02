<template>
    <select v-model="selectArtist"
    @change="$emit('filter',selectArtist)"
    class="inputSelect ms-4" name="genre" id="pet-select">
        <option value="">Please choose an author</option>
        <option value="Bon Jovi">Bon Jovi</option>
        <option value="Queen">Queen</option>
        <option value="Sting">Sting</option>
        <option value="Steve Gadd Band">Steve Gadd Band</option>
        <option value="Iron Maiden">Iron Maiden</option>
        <option value="Eric Clapton">Eric Clapton</option>
        <option value="Deep Purple">Deep Purple</option>
        <option value="Metallic">Metallic</option>
        <option value="Dave Weckl">Dave Weckl</option>
        <option value="Michael Jacjson">Michael Jacjson</option>

            
    </select>
</template>

<script>




export default {
    name: 'OptionsAuthor',
     
    
    components: {
        
    
        
    },
    data() {
      return {
          
          selectArtist:'',

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