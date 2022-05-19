<template>
  <div class="up d-flex">
      <i class="fa-brands fa-spotify"></i>
      <select class="form-select rl-select" name="generi" >
        <option selected>Seleziona un genere</option>
        <option value="1">Rock</option>
        <option value="2">Pop</option>
        <option value="3">renatoseiuncoglione</option>
        <option value="4">Seleziona un genere</option>
      </select>
    </div>
</template>

<script>
export default {
  name: "SelectComp"
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
