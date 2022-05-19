<template>
  <div class="up d-flex">
      <i class="fa-brands fa-spotify"></i>
      <select v-model="genreToSearch" class="form-select rl-select" name="generi" >
        <option value="" selected>Seleziona un genere</option>
        <option value="Rock">Rock</option>
        <option value="Pop">Pop</option>
        <option value="Jazz">Jazz</option>
        <option value="Metal">Metal</option>
      </select>
    </div>
</template>

<script>
export default {
  name: "SelectComp",
  data(){
    return{
      genreToSearch: ""
    }
  }
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
    padding: 5px 12px;
    border-radius: 5px;
    font-size: 12px;
  }
}
</style>
