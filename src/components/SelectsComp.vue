<template>
  <div class="up d-flex">
      <i class="fa-brands fa-spotify"></i>
      <div class="selects d-flex">

        <select v-model.trim="albumChosed" @change="$emit('albumSearching', albumChosed)" class="form-select rl-select" name="genre" >
          <option value="">Seleziona un Album</option>
          <option value="New Jersey">New Jersey</option>
          <option value="Live at Wembley 86">Live at Wembley 86</option>
          <option value="Ten's Summoner's Tales">Ten's Summoner's Tales</option>
          <option value="Steve Gadd Band">Steve Gadd Band</option>
          <option value="Brave new World">Brave new World</option>
          <option value="One more car, one more raider">One more car, one more raider</option>
          <option value="Made in Japan">Made in Japan</option>
          <option value="And Justice for All">And Justice for All</option>
          <option value="Hard Wired">Hard Wired</option>
          <option value="Bad">Bad</option>
        </select>

        <select v-model.trim="genreChosed" @change="$emit('genreSearching', genreChosed)" class="form-select rl-select" name="genre" >
          <option value="">Seleziona un Genere</option>
          <option value="Rock">Rock</option>
          <option value="Pop">Pop</option>
          <option value="Jazz">Jazz</option>
          <option value="Metal">Metal</option>
        </select>

      </div>
      
    </div>
</template>

<script>
export default {
  name: "SelectsComp",

  data(){
    return{
      genreChosed: "",
      albumChosed: ""
    }
  },
}
</script>

<style lang="scss" scoped>
.up{
  width: 100%;
  height: 50px;
  background-color: #2e3a46;
  justify-content: space-between;
  align-items: center;
  padding: 10px;
  i{
    color: #34be58;
    font-size: 30px;
  }
  .rl-select{
    width: 170px;
    border: none;
    margin: 10px;
    padding: 5px 12px;
    border-radius: 5px;
    font-size: 12px;
  }
}
</style>
